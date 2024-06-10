# RL
Reinforcement Learning Project
Pong Agent
### Übersicht
Dieses Projekt implementiert einen Pong-Agenten mithilfe von Reinforcement Learning (RL). Der Agent wird mithilfe von Deep Q-Learning (DQN) trainiert, das klassische Atari-Spiel Pong zu spielen. Das Hauptziel dieses Projekts besteht darin, die Anwendung von RL-Techniken zu demonstrieren, um einen KI-Agenten zu trainieren, in einer Spielumgebung eine hohe Leistung zu erzielen.

![PongEnvironment](https://github.com/alexx1374/RL/assets/104265677/cd0cdf2b-7aa1-4fc3-b0f3-3b3515cc803c)



### Funktionen
Deep Q-Network (DQN)-Implementierung: Verwendet ein neuronales Netzwerk, um die Q-Wert-Funktion anzunähern.
Experience Replay: Verwendet einen Wiedergabepuffer, um vergangene Erfahrungen für das Training zu speichern und wiederzuverwenden.
Zielnetzwerk: Implementiert ein separates Zielnetzwerk, um das Training zu stabilisieren.
OpenAI Gym-Integration: Verwendet die OpenAI Gym-Umgebung für das Pong-Spiel.
Framework: ALE/Pong-v5

### Setup
#### Repository klonen:
```shell
git clone https://github.com/alexx1374/RL.git
```
#### Virtuelle Umgebung erstellen (optional): 
```shell
python -m venv venv
```
Virtuelle Umgebung Starten:
```shell
venv\Scripts\activate
```
#### Die erforderlichen Pakete installieren:
```shell
pip install -r requirements.txt
```
#### Agenten trainieren

python train.py ???????????

Dadurch wird der Trainingsprozess gestartet und das trainierte Modell im Verzeichnis gespeichert.

Den Agenten auswerten
Um die Leistung eines trainierten Agenten auszuwerten, führen Sie Folgendes aus:
python evaluate.py --model_path models/pong_dqn.h5


### Ergebnisse
Während des Trainings wird alle 25 Episoden ein Plot ausgegeben, welcher den Punktestand die Episodenlänge, den Verlust und den Epsilonwert ausgibt. Diese Plots werden gespeichert und der Trainingsverlauf kann dadurch verfolgt werden.
Nach mehreren Tagen Training und 1000 trainierten Episoden ist folgendes Ergebnis rausgekommen.

![pong_Plot_episode_1000](https://github.com/alexx1374/RL/assets/104265677/f49dfe04-0404-4785-ab6e-9769aa6391b4)

### Referenzen
Deep Q-Learning mit TensorFlow und Keras
OpenAI Gym-Dokumentation

### Lizenz
Dieses Projekt ist unter der MIT-Lizenz lizenziert – Einzelheiten finden Sie in der Datei LICENSE.
