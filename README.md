Running Google Assistant as a Systemd unit

Ensure you have Google Assistant setup using [this guide](https://www.xda-developers.com/how-to-get-google-assistant-on-your-windows-mac-or-linux-machine/)

Replace ~/.local/lib/python3.5/site-packages/googlesamples/assistant/\__main__\.py with mine. 

I have removed the need to press the "Enter" key, which makes it "Always listening". 


The below commands will allow Google Assistant to start on boot using systemd. 
```bash
cp google_assistant.service ~/.config/systemd/user/default.target.wants/
systemctl --user daemon-reload 
systemctl --user start google_assistant.service 
systemctl --user enable google_assistant.service  #Use this command only if you would like it to start on boot
```


`I have no gurantee it will work on later versions of assistant.`


Google assistant is the trademark of Google Inc., I owned no rights to any of their products or their trademark.
