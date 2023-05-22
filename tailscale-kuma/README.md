# Why a seperate compose for tailscale?

I run Tailscale/Kuma on a seperate VirtualMachine then the rest of the services. This is because some of the services (Traefik and PiHole) are using macvlan for direct LAN access. Macvlan however does not allow localhost communication to the container through the host machine - which Tailscale requires.

TLDR: Tailscale on a seperate VM allows me to have the most optimal setup.