When you clone your linux machine in an image you also clone Anydesk's configuration and id, so if you boot a clone of your machine it starts using your Anydesk id making all the other cloned installations unreachable.

Запустите это на своих клонах, чтобы сбросить идентификатор и пароль Anydesk.
```
wget --no-cache -O /tmp/reset_anydesk_id.sh https://raw.githubusercontent.com/Antiavk/linux_reset_anydesk_id/master/reset_anydesk_id.sh && sudo chmod +x /tmp/reset_anydesk_id.sh && sudo /tmp/reset_anydesk_id.sh
```

Also restarts lightdm service to allow remote connection without reboot in Raspbian

Warning: Anydesk options are completely resetted and then remote access password is configured. You lose other customizations if you run this
