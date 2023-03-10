# chatgpc-cli
ChatGPC Natural language Command Line Interface

## Quick Setup

1. Setup virtual environment and install `source .venv/bin/activate && pip install -e .`
2. Register for an account on OpenAI https://beta.openai.com
3. Create API key at https://beta.openai.com/account/api-keys'
4. Add key to shell config so for zshell `echo export OPENAI_API_KEY=NEW_KEY >> ~/.zshrc`
5.  bin/chatgpc PROMPT

## Example Use Cases

```
$ bin/chatgpc git log pretty
>>> Run:  git log --pretty=format:"%h %ad | %s%d [%an]" [y/N]: y
$ git log --pretty=format:"%h %ad | %s%d [%an]"

$  bin/chatgpc set kubernetes namespace
>>> Run:  kubectl config set-context default --namespace=kube-system [y/N] y
$ kubectl config set-context default --namespace=kube-system

$  bin/chatgpc exec into the docker image called foobar
>>> Run:  docker exec -it foobar bash [y/N]: y
$ docker exec -it foobar bash
```

## Background
Simple cli wrapper for OpenAI's ChatGPC which was created from the Natural Language shell tutorial  https://openai.com/blog/openai-api/