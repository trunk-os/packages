include ../include.mk

pre-down:
	rm -rf /tmp/buckle

run: down
	sudo podman run -it -d --privileged --name "$(NAME)" --net bridge --device /dev/zfs --pid host -v /trunk:/trunk:shared -v /var/run/dbus:/var/run/dbus -v /var/log/journal:/var/log/journal:ro -v /run/log/journal:/run/log/journal:ro -v /run/systemd:/run/systemd:ro "$(LATEST_TAG)"
