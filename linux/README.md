# Linux tips

## Enable sleep mode
```bash
sudo systemctl unmask sleep.target suspend.target hibernate.target hybrid-sleep.target```


## Disable sleep mode
```bash
sudo systemctl mask sleep.target suspend.target hibernate.target hybrid-sleep.target```
