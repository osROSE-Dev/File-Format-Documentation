# VFS - Virtual File System

The VFS is used to store most files used by the client.

## Pseudo format
```
uint16 installationVersion
uint16 currentVersion
uint32 vfsCount

for vfsCount
    int16 vfsNameLength
    char vfsName[vfsNameLength]
    uint32 vfsIndexOffset

for vfsCount
    # VFS Header
    uint32 fileCount
    uint32 fileDeletedCount
    uint32 vfsStartOffset
    
    for fileCount
        int16 fileNameLength
        char filename[fileNameLength]
        uint32 fileOffset
        uint32 fileSize
        uint32 blockSize
        boolean deleted
        uint8 compressType
        uint8 encryptionType
        uint32 fileVersion
        uint32 crc32Checksum
```

## Enums

```

enum CompresType
{
    UNCOMPRESSED,
    ZIP,
}

enum EncryptedType
{
    NONE = 0,
    ENCRYPTED,
}
```