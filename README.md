# SHIELD Cassandra Add-on

This BOSH release provides add-on plugin for augmenting SHIELD
Agents with Cassandra backup and restore possibilities.

## Versions

The following versions are currently available:

 - **2b5dfda** via `shield-addon-cassandra-pluggin`

## Using this BOSH Release

**Note:** This BOSH release is not intended to stand on its own.
It exists to augment the `shield-agent` job of the [SHIELD BOSH
Release][1], and only in cases where cassandra support is necessary.

To colocate this BOSH release with your shield-agent instance
group, just add a new job to the group:

```yaml
instance_groups:
  - name: whatever
    jobs:
      # ...
      - name:    shield-addon-cassandra-plugin
        release: shield-addon-cassandra
```

That's really all there is to it.

[bug]: https://github.com/orange-cloudfoundry/shield-addon-cassandra-boshrelease/issues
[1]:   https://github.com/starkandwayne/shield-boshrelease