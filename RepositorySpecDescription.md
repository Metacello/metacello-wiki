## Common descriptions ##
  * MCDirectoryRepository on FileDirectory
```
spec repository: '/opt/mc/repository'.
spec repository: 'c:\pharo\myapp\repo\'.
```
  * MCDictionaryRepository
```
spec repository: 'dictionary://GlobalName'.
```
  * MCHttpRepository
```
spec repository: 'http://www.example.com/rr';
spec repository: 'http://www.example.com/private' username: 'foo' password: 'bar'.
```
## Squeak/Pharo-specific descriptions ##
    * MCFtpRepository
```
spec repository: 'ftp://ftp.example.com/repo'.
```
## GemStone-specific descriptions ##
  * MCDirectoryRepository on ClientFileDirectory
```
spec repository: 'client:///opt/mc/repository'.
```
  * MCDirectoryRepository on ServerFileDirectory
```
spec repository: 'server:///opt/mc/repository'.
```