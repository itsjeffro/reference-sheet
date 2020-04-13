# Memory

## Checking memory

```bash
free -h
```

Output:

```bash
              total        used        free      shared  buff/cache   available
Mem:           1.9G        462M        236M         12M        1.3G        1.3G
Swap:          2.0G          0B        2.0G
```

|name|description|
|----|-----------|
| free | The amount of memory which is currently not used for anything. This number should be small, because memory which is not used is simply wasted |
| available | The amount of memory which is available for allocation to a new process or to existing processes |
