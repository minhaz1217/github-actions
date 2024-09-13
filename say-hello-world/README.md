## If this is the problem
```
docker: Error response from daemon: failed to create task for container: failed to create shim task: OCI runtime create failed: runc create failed: unable to start container process: exec: "/entrypoint.sh": permission denied: unknown.
```

Then >> 

## To change the permission
```
git add entrypoint.sh
git update-index --chmod=+x entrypoint.sh
```


## Inputs

## `who-to-greet`

**Required** The name of the person to greet. Default `"World"`.

## Outputs

## `time`

The time we greeted you.

## Example usage

uses: actions/hello-world-docker-action@v2
with:
  who-to-greet: 'Mona the Octocat'