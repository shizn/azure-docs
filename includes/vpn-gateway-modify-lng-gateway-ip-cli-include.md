### To modify the local network gateway gatewayIpAddress

If the VPN device that you want to connect to has changed its public IP address, you need to modify the local network gateway to reflect that change. The gateway IP address can be changed without removing an existing VPN gateway connection (if you have one). To modify the gateway IP address, replace the values 'Site2' and 'TestRG1' with your own using the [az network local-gateway update](https://docs.microsoft.com/cli/azure/network/local-gateway#update) command.

```azurecli
az network local-gateway update --gateway-ip-address 23.99.222.170 -n Site2 -g TestRG1
```

Verify that the IP address is correct in the output:

```
"gatewayIpAddress": "23.99.222.170",
```