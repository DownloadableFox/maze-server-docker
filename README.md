# Maze Server

An experimental server for LiveOverflow's game "Maze", which was developed as part of the CSCG 2020. 
If everything goes to plan, the code in this repository will soon be run on a DigitalOcean server for everyone interested to try out.

## Update

Unfortunately, there is no public server anymore, but you can still run one locally or even publicly yourself.

## Features

- [x] Basic functionality of the game such as moving around and showing emojis
- [x] Multiplayer support for the features above
- [x] Unlocking of emojis and places
- [x] Fur colors
- [x] Teleporting to places
- [x] "Anti Cheat" for passing through walls
- [x] "Anti Cheat" for speed hax
- [x] Dying due to lava
- [x] Race support
- [x] Flags
- [x] White Rabbit Bot
- [x] Highscore board
- [ ] Proper Anti-DDos


## Instructions for running locally

Please clone the repository and build & run the the two projects inside with `cargo run --release`.
Please note that you need the nightly version of rustc to compile the master server.
If you are on Linux, run these two commands to redirect the traffic to the locally running servers :

`sudo iptables -t nat -I OUTPUT -p udp -d 147.75.85.99 --dport 1337:1357 -j DNAT --to-destination 127.0.0.1:1337`   
`sudo iptables -t nat -I OUTPUT -p tcp -d 147.75.85.99 --dport 80 -j DNAT --to-destination 127.0.0.1:8000`

