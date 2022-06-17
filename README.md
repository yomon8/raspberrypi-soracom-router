Build Wifi Router with Raspberry Pi and SORACOM Air SIM
---


![](./image.png)


### Requirements

- Raspberry Pi 3 / 4 with USB SIM Dongle
- SORACOM SIM
- Rapsberry Pi OS
- SSH configured


### How To Install

install python package and activate virtual env.

```sh
poetry install
poetry shell
```


install soracom router on raspberry pi

```sh
# ip address for your Raspberry Pi 
ROUTER_HOST_IP=xxx.xxx.xxx.xxx

# SSID for Raspberry Pi router
SSID=raspberrypi

# pass phrase length must be 8..63
WPA_PASS=abcdefgh 
ansible-playbook -i ${ROUTER_HOST_IP}, -e ssid=${SSID} -e wpapass=${WPA_PASS} ./soracom_router.yaml
```


