Experimental.

To use this with [Enterprise Contract](https://enterprisecontract.dev/):

```
ec validate image --image $IMAGE_REF --policy github.com/simonbaird/securesign-ec-config?ref=main
```

Notes:
* It's not required that the policy-data directory and the policy.yaml file
  are in the same repo, but note that the data source in policy.yaml should
  point to wherever the policy-data is placed.
* It's also not required that the policy.yaml file is placed in its own git repo.
  It could be placed somewhere else.
* If it's placed in a subdirectory, the `//` separator can be used, e.g.
  `--policy github.com/some-org/some-repo//path/to/dir?ref=someref`
* EC looks for one of `./policy.yaml` or `./.ec/policy.yaml` at the given
  location, so you could put a `.ec` directory in the top level of a git repo
  and place a `policy.yaml` there for example.
* For either of these files, JSON should work the same as YAML.
