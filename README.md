### install 
1. install docker
2. run ```docker compose up --build```

### service
- open webui chat : http://localhost:8080/
    - add model ```docker exec -it ollama ollama run <model_name>```
    - go to bash ollama ```docker exec -it ollama /bin/bash```

- jupyter notebook : http://localhost:8881/
- redis insight : http://localhost:8001/