# docker-tutorial

Code that goes with the mlibrary [Getting Started with Docker and Docker Compose](
https://mlit.atlassian.net/wiki/spaces/LD/pages/2404090314/Getting+Started+with+Docker+and+Docker-Compose) tutorial

## Set up

Run the setup script
```
./init.sh
```

This will:

* copy `env.example` to `.env` 
* enable the precommit hook which wil lint the code before committing.  Uncomment
  those lines in `.git/hooks/precommit` to enable running tests.
* build the docker image
* install the gems

The script does not overwrite `.env` or `/git/hooks/precommit`.

## Tests
This has rspec initialialized and has one sample test in `spec/sample_spec.rb`. 

A github actions workflow is included that runs standard linting and the tests
