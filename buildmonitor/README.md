# Raspberry Pi Build Monitor

Follow [this excellent guide](http://archlinuxarm.org/platforms/armv6/raspberry-pi) to prepare the Pi.

Update the inventory.

```
$ vim rpis
```

Run these commands.

```
$ ansible-playbook -i rpis bootstrap.yml --limit buildmonitor.leslieianson.com
$ ansible-playbook -i rpis buildmonitors.yml
$ ansible -i rpis buildmonitor.leslieianson.com -a "shutdown -r now"
```

Job done.
