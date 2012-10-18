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

    
