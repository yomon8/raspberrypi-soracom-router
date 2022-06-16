Build Wifi Router with Raspberry Pi and SORACOM Air SIM
---

install python package and activate virtual env.

```sh
poetry install
poetry shell
```


install soracom router on raspberry pi

```sh
SSID=raspberry
WPA_PASS=abcdefcg # pass phrase length must be 8..63
ROUTER_HOST_IP=192.168.11.62
ansible-playbook -i ${ROUTER_HOST_IP}, ./soracom_router.yaml
ansible-playbook -i ${ROUTER_HOST_IP}, -e ssid=${SSID} -e wpapass=${WPA_PASS} ./soracom_router.yaml
```


