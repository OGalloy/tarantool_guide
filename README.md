## tarantool_guide

### Create  tarantool container
```bash
docker run \
--name mytarantool \
-d -p 3301:3301 \
-v /data/dir/on/host:/var/lib/tarantool \
tarantool/tarantool:latest
```
### Attaching to tarantool

```bash
docker exec -i -t mytarantool console
```
### Set console output
```bash
#lua-style
\set output lua
#yaml-style
\set output yaml 
```
```bash
### Set language
\set language sql
#or lua
\set language lua
```