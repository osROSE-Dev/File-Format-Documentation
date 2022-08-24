# AIP - AI Program

# Pseudo file format

```c
char programName[33]

# conditions
int32 conditionCount
for conditionCount
    uint32 blockSize
    uint32 conditionType
    data[blocksize - sizeof(uint32 * 2)]
    
# actions
int32 actionCount
for actionCount
    uint32 blockSize
    uint32 actionType
    data[blocksize - sizeof(uint32 * 2)]
    
```

# Action and condition types
And overview of all data mined ai conditions and actions can be found in the respective folders;

* [Actions](aip/actions.md)
* [Conditions](aip/conditions.md)
