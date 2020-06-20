# go-makefile

Makefile helpers for GO.

## Project structure

```.sh
├── .project
│   ├── yaml.sh             # yaml parser
│   ├── config_var.sh       # extract yaml config variable
│   └── go-project.mk       # include into your Makefile using $GOPATH
│   └── gomod-project.mk    # include into your Makefile using go mod
├── .VERSION                # version of your project
├── config.yml              # config
└── Makefile                # Makefile
```

## How to use

- Copy `.project` folder to your project's root folder
- Create `.VERSION` file in the root of your project
- Create `config.yml` file in the root of your project
- Create `Makefile`
    - `include .project/go-project.mk` with projects using $GOPATH
    - `include .project/gomod-project.mk` with projects using `go mod`

## Common commands

- `make vars` - print make variables
- `make env` - pring GO environment
- `make generate` - generate GO files
- `make lspkg` - list GO packeges in the current project
- `make bench` - GO test with bench
- `make fmt` - run `go fmt` on project files
- `make vet` - run `go vet` on project files
- `make lint` - run `go lint` on project files
- `make test` - run test
- `make testshort` - run test with -short flag
- `make covtest` - run test with coverage report
- `make coverage` - open coverage report
- `make coveralls` - publish coverage to coveralls"

## Coverage report

Install `cov-report` in your project:

    go get github.com/go-phorce/cov-report/cmd/cov-report