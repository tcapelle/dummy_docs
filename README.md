# Automatic Translation using GPT

This repo implements automatic translation of a folder containing markdown files using GPT-3/4. This is done by using the github action (and python lib) [gpt-translate](https://github.com/tcapelle/gpt_translate) and the defined [workflow file](/.github/workflows/main.yml) in this repo.

## Try it yourself

The workflow is triggered when you merge a PR to the `main` branch and that PR contains modifies markdown files. The workflow will then create a new PR with the translated files. You can try it yourself by creating a PR to this repo and modifying the files in the `docs` folder.

You could modify the workflow so it triggers on prs or when specific tags are pushed to the repo.

## How it works

The main step is performing the translation, this is configured in the workflow file:

```yaml
uses: tcapelle/gpt_translate@v1.0
env:
    OPENAI_API_KEY: ${{ secrets.OPENAI_API_KEY }}  # you need to provide an OPENAI_API_KEY in your secrets
    WANDB_API_KEY: ${{ secrets.WANDB_API_KEY }} # you need to provide a secret containing output of https://wandb.ai/authorize
with:
    folder-to-translate: 'docs/' # the folder where the markdown files are located
    language: "es" # the language to translate
    output-folder: "docs-es/" # the output folder where the translated files will be stored
    input-file: ${{ inputs.input_file }} # list of modified .md/.mdx files to translate
```

You also need to setup a [configs](/configs/) folder in your repo to setup the specifics on how the translation is performed. Inside this folder you have the following structure:

```
├── configs
│   ├── human_prompt.txt  # the prompt to use to translate the files
│   ├── language_dicts    # the dictionaries to use for each language
│   │   ├── es.yaml       # the dictionary for the spanish language
│   │   └── ja.yaml       # the dictionary for the japanese language
│   ├── model_config.yaml # the model configuration to use, supports openai.Completion api parameters
│   └── system_prompt.txt # the system prompt to inject to the chat
```

We only translate files on the PR that live inside the `folder-to-translate` and that are of type markdown.

After the translation is completed, a PR is created with the translated files. The PR is created using the [create-pull-request](https://github.com/peter-evans/create-pull-request/blob/main/docs/examples.md) action. By default it creates a new branch with the translated files and creates a PR to merge that branch to the `main` branch. You can modify the action to create the PR to a different branch or to a different repo.

