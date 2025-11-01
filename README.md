# all-one-unix-homescreen-learnable-cheat-sheet
Each line has everything you'll need to know to be a terminal wizard and fits on your phone home screen.

# SEARCH / INSPECT
grep -Rni "err" . | less        # find + case-ins + lines + scroll
grep -Rnw "token" --include="*.js" src/  # exact word in .js only
find . -type f -mtime -1 -name "*.log"   # files changed last 24h
tail -f app.log | grep "WARN"   # live log filter
rg "auth" -g "*.js"             # fast search JS only (ripgrep)

# FILE DEBUG
wc -l file                      # count lines
diff -u old new | less         # unified diff scrollable
du -sh * | sort -h              # directory sizes sorted
less +F log.txt                 # follow file but scrollable

# PROCESS / BACKGROUND
nohup cmd > out.log 2>&1 &      # run forever, detach, log all
cmd & disown                    # background + free shell
ps aux | grep "[n]ode"          # find process cleanly

# SPEED / RECALL
history | grep ssh              # find cmd by pattern
Ctrl+R (reverse search)         # brain expansion mode
