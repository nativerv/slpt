# `slpt` - simple (suckless) OpenAI ChatGPT client written in POSIX shell

## Synopsis

`slpt <prompt>`

## Description

A CLI client for <https://api.openai.com>.

You need to provide an environment variable containing a command that would retrieve the password. See [Environment Variables](#environment-variables).

## Dependencies

- `curl`
- `jq`

## Examples

```
$ slpt mass of the sun
The mass of the sun is approximately 1.989 x 10^30 kilograms.
$ slpt give me example of if in posix shell without explanation
if [ -f myfile.txt ]; then
   echo "File exists!"
fi
```

## Environment variables

- `SLPT_API_KEY_COMMAND` a command that retrieves the API key that you get from <https://beta.openai.com/account/api-keys>. Can be a simple `echo mypassword`, but useful with password managers like the [pass](https://www.passwordstore.org).

## TODO

- [ ] Session (chat) support
- [ ] Caching of responses for the same query
- [ ] Flags and environment vars for `model`, `temperature` and `top_probability` (`top_p`)
