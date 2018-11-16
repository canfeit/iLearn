```bash
brew services start rethinkdb
echo 'export PATH="/usr/local/opt/sqlite/bin:\$PATH"' >> ~/.bash_profile
export LDFLAGS="-L/usr/local/opt/sqlite/lib"
export CPPFLAGS="-I/usr/local/opt/sqlite/include"
export PKG_CONFIG_PATH="/usr/local/opt/sqlite/lib/pkgconfig"
```
