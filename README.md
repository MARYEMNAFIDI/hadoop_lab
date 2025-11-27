# TP Docker + Hadoop HDFS

Ce TP a pour objectif d’installer un mini-cluster Hadoop via Docker, puis de manipuler HDFS.
Il permet de comprendre la structure d’un cluster Hadoop, la gestion NameNode / DataNode et les commandes HDFS essentielles.

## 📁 Structure du projet

tp-docker-hadoop/
│
├── README.md
├── commands.md
├── docker/
│   └── docker-compose.yml
├── data/
│   ├── purchases.txt
│   
├── scripts/
│   ├── hdfs_create_dirs.sh
│   ├── hdfs_put_files.sh
│   └── hdfs_list.sh


## 🐳 Démarrage du Cluster Hadoop

```bash
docker-compose -f docker/docker-compose.yml up -d
```

## 🔍 Vérifier les conteneurs

```bash
docker ps
```

## 🌐 Interface Web Hadoop NameNode

http://localhost:9870

## 🐘 Commandes HDFS

```bash
hdfs dfs -mkdir /user/test
hdfs dfs -ls /
hdfs dfs -put data/exemple1.txt /user/test/
hdfs dfs -get /user/test/exemple1.txt .
hdfs dfs -rm /user/test/exemple1.txt
```

## 📜 Scripts inclus

- hdfs_create_dirs.sh : crée les répertoires HDFS
- hdfs_put_files.sh : upload automatique des fichiers
- hdfs_list.sh : liste les fichiers du dossier HDFS

## 📦 Auteur
TP Hadoop Docker - Version prête à l’utilisation.
