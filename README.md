# Opscode rebar templates #

## Install ##

Clone this repo into `~/.rebar/templates/opscode` like this:

    mkdir -p ~/.rebar/templates/
    cd ~/.rebar/templates
    git clone git@github.com:opscode/opscode-rebar-templates.git opscode

## Generate a new Erlang project ##

The `project` template creates a skeleton Erlang OTP application (not
a top-level OTP Release project). Use it like this:

    mkdir my_proj
    cd my_proj
    rebar create template=project name=my_proj \
      description="describe it, yo" \
      author_name="First Last" \
      author_email="you@opscode.com"

## Generate a new Erlang top-level OTP release project ##

The `rel_project` template creates a skeleton of an Erlang OTP
embedded release application. By default, this assumes no local source
code. It should do the right thing, however, if add a `src`
directory. This setup does not work with the `apps/APP` structure.

    mkdir my_rel
    cd my_rel
    rebar create template=project name=my_rel \
      description="describe it, yo" \
      author_name="First Last" \
      author_email="you@opscode.com"
    make prepare_release

## License ##

Apache 2. See [LICENSE](./LICENSE).
