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

```
