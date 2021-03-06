# TsungDemo

Demo to test Tsung with.

## Building

```
# Set env vars
mix phx.gen.secret

# Initial setup
mix deps.get --only prod
MIX_ENV=prod mix compile

# Build release
MIX_ENV=prod mix release
```

Now you can .tar.gz the `_build/prod/rel/tsungdemo` directory and ship it:
```
tar -zcvf tsungdemo.tar.gz _build/prod/rel/tsungdemo
```

And extract it on the server:
```
tar -zxvf tsungdemo.tar.gz
```

## Running

`SECRET_KEY_BASE=YOURSECRETKEY _build/prod/rel/tsungdemo/bin/tsungdemo start --erl "+P 5000000"`

Or if the --erl flag doesn't work with releases, add +P 5000000 to the vm.args file.

## Phoenix

To start your Phoenix server:

  * Setup the project with `mix setup`
  * Start Phoenix endpoint with `mix phx.server`

Now you can visit [`localhost:4000`](http://localhost:4000) from your browser.

Ready to run in production? Please [check our deployment guides](https://hexdocs.pm/phoenix/deployment.html).

## Learn more

  * Official website: https://www.phoenixframework.org/
  * Guides: https://hexdocs.pm/phoenix/overview.html
  * Docs: https://hexdocs.pm/phoenix
  * Forum: https://elixirforum.com/c/phoenix-forum
  * Source: https://github.com/phoenixframework/phoenix
