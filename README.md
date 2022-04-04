Kanban-доска Restyaboard (аналог Trello) в связке с обратным прокси Traefik


На DNS-хостинге прописать запись типа А:

    restyaboard.hostname.com		IP
    
Далее

    git clone ${this repo}

    cd restyaboard
    touch acme.json
    chmod 600 acme.json
    mkdir db
    
    
Создать свой .env файл с переменными окружения из .env-default и подправить значения на свои

    cp .env-default .env
    
Старт

    sudo docker-compose -f docker-compose-restya.yml -f docker-compose-traefik.yml up -d
    
В браузере
    
    restyaboard.hostname.com
