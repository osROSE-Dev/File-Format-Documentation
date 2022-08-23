# STB - String Table

## Pseudo format
```
uint8 version[4]
uint32 dataOffset
int32 rowCount
int32 columnCount

# Table sizing
int32 lineHeight
int16 defaultColumnWidth 
if version[3] == '1'
    for columnCount
        uint16 columnWidth

// Column names
for columnCount
    int16 stringLength
    char columnName[stringLength]


// Row names
int16 stringLength
char rowTitleColumnName[stringLength]

for rowCount - 1
    int16 stringLength
    char rowTitleColumnName[stringLength]

for rowCount - 1
    for colCount - 1
        int16 stringLength
        char cellValue[stringLength]
```
