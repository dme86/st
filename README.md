# st - simple terminal

This is my customized version of the [Suckless Simple Terminal](https://st.suckless.org/), tailored to meet my specific requirements.

To install it on a Linux system with Xserver, please clone this repository and execute the command 

`sudo make install`.

Scrollback functionality can be accessed using `Shift` + `PgUp/PgDn`.

The output of the last shell command can be copied with `Ctrl` + `Shift` + `Y`.
For fish, add these hooks to `~/.config/fish/config.fish`:

```fish
function __st_cmd_start --on-event fish_preexec
    printf '\e]777;cmd-start\a'
end

function __st_cmd_end --on-event fish_postexec
    printf '\e]777;cmd-end\a'
end
```

| st |
|--|
| ![](https://i.imgur.com/XnoHRMX.png) |
