# sboardwell-bundles-test

## Commands for Demo

```sh
# after checking out, copy the example files
❯ cp -r ../ci-bundle-utils/examples/example-bundles-repo/bundles .
❯ cp -r ../ci-bundle-utils/examples/example-bundles-repo/bundle-profiles.yaml .
❯ cp -r ../ci-bundle-utils/examples/example-bundles-repo/transformations .
❯ cp -r ../ci-bundle-utils/examples/example-bundles-repo/Makefile .

# add a profile and empty bundle.yaml
touch bundles/controller-bundles/controller-a/bundle.yaml
vi bundle-profiles.yaml

# you should have something like this
❯ tree
.
├── bundle-profiles.yaml
├── bundles
│   └── controller-bundles
│       ├── controller-a
│       │   └── bundle.yaml
│       └── Makefile
├── Makefile
├── README.md
└── transformations
    ├── controllers-common.yaml
    └── remove-dynamic-stuff.yaml

# Variables needed for docker

# create an API token at OC level
export BUNDLEUTILS_USERNAME=<your-user> # reminder we can use a service user with fine grained permissions later in prod
export BUNDLEUTILS_PASSWORD=<your-token> #  # reminder we can use a service user with fine grained permissions later in prod

# the single user wildcard license
export CASC_VALIDATION_LICENSE_KEY_B64=$(cat license.key | base64 -w0)
export CASC_VALIDATION_LICENSE_CERT_B64=$(cat license.cert | base64 -w0)

# the full path to your bundle. e.g.
BUNDLES_WORKSPACE=/home/user/Workspace/tsmp-falcon-platform/sboardwell-bundles-test

# now follow instructions 
```
