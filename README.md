==================================================================
                  HADOOP LAB - MAPREDUCE AVEC MAVEN
                  Auteur : Maryem NAFIDI
                  GitHub : https://github.com/MARYEMNAFIDI/hadoop_lab
                  Date   : Novembre 2025
==================================================================

Description
-----------
Ce dépôt contient mon laboratoire Hadoop MapReduce complet réalisé avec Maven.
Le projet traite des fichiers d’entrée (listés dans inputFiles.lst) et génère
des résultats (fichiers de sortie listés dans createdFiles.lst).

Contenu du dépôt
----------------
- pom.xml                → Configuration Maven + dépendances Hadoop
- src/main/java/         → Code source Java (Mapper, Reducer, Driver)
- inputFiles.lst         → Liste des fichiers d’entrée utilisés
- createdFiles.lst       → Liste des fichiers de sortie générés
- README.txt             → Ce fichier
- .gitignore             → Ignore les fichiers temporaires et les builds
- .gitattributes         → Support Git LFS si besoin

Comment exécuter le projet (mode local / standalone)
----------------------------------------------------
1. Cloner le dépôt
   git clone https://github.com/MARYEMNAFIDI/hadoop_lab.git
   cd hadoop_lab

2. Compiler avec Maven
   mvn clean package

3. Lancer le job MapReduce
   hadoop jar target/hadoop-lab-1.0-SNAPSHOT.jar com.tonpackage.TonDriverClasse chemin/input chemin/output

   (Remplace com.tonpackage.TonDriverClasse par le vrai nom de ta classe Driver)

Exemple concret
---------------
hdfs dfs -mkdir /input
hdfs dfs -put inputFiles.lst /input/

hadoop jar target/hadoop-lab-1.0-SNAPSHOT.jar com.tonpackage.TonDriverClasse /input /output

hdfs dfs -cat /output/part-r-00000

Technologies utilisées
----------------------
- Apache Hadoop 3.x
- Apache Maven
- Java 8 ou supérieur

