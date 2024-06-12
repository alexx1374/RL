# RL
Reinforcement Learning Project
Pong Agent

<img src="https://github.com/alexx1374/RL/assets/104265677/ed76aa46-4689-4104-9471-7f2cfcb196bf" width="500"/> 
<img src="https://github.com/alexx1374/RL/assets/104265677/eb9e4a27-55a8-49c4-8813-69605ef521e6" width="500"/>

Unterschied zwischen der ersten und nach über 700 Epochen. (Braun: Spieler 1, Grün: RL-Agent)

### Übersicht
Dieses Projekt implementiert einen Pong-Agenten mithilfe von Reinforcement Learning (RL). Der Agent wird mithilfe von Deep Q-Learning (DQN) trainiert, das klassische Atari-Spiel Pong zu spielen. Das Hauptziel dieses Projekts besteht darin, die Anwendung von RL-Techniken zu demonstrieren, um einen KI-Agenten zu trainieren, in einer Spielumgebung eine hohe Leistung zu erzielen.

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
### Training
Der Code wurde 1000 Episoden lang trainiert. Dabei wurden folgende Hyperparameter verwendet:
- learning_rate = 0.0001
- discount_factor = 0.99
- epsilon = 1.0
- epsilon_decay = 0.995
- epsilon_min = 0.01
- batch_size = 64
- num_episodes = 1000



Um das Training zu verfolgen wurden folgende Maßnahmen durchgeführt:
Beim Training des Codes wird für jede Episode ein Video aufgenommen und (theoretisch) im ["train_videos"](https://github.com/alexx1374/RL/tree/dev/data/train_videos) Ordner gespeichert. (Den Upload der Videos auf GitHub habe ich nicht durchgeführt, sondern nur Beispielvideos in den Ordner ["best_videos"](https://github.com/alexx1374/RL/tree/dev/data/best_videos) geladen.)
Des Weiteren wird immer das Model mit dem besten Reward gespeichert. Um gezielt Evaluierungen durchzuführen wurde alle 100 Episoden ein weiteres Model gespeichert. Die Models können im Ordner ["models"](https://github.com/alexx1374/RL/tree/dev/models) abgerufen werden.

### Ergebnisse
Während des Trainings wird alle 25 Episoden ein Plot ausgegeben, welcher den Punktestand die Episodenlänge, den Verlust und den Epsilonwert ausgibt. Diese Plots werden im Ordner ["plots"](https://github.com/alexx1374/RL/tree/dev/data/plots) gespeichert und der Trainingsverlauf kann dadurch verfolgt werden.
Nach mehreren Tagen Training und 1000 trainierten Episoden ist folgendes Ergebnis rausgekommen.

![pong_Plot_episode_1000](https://github.com/alexx1374/RL/assets/104265677/f49dfe04-0404-4785-ab6e-9769aa6391b4)

### Evaluierung
Für die Evaluierung wurde eine Länge von 10 Episoden gewählt und das fertig trainierte Model wurde geladen und evaluiert. Außerdem wurden noch einmal für alle 10 Episoden ein Video, sowie ein Plot erstellt und im Ordner ["plots"](https://github.com/alexx1374/RL/tree/dev/data/plots) und ["eval_videos"](https://github.com/alexx1374/RL/tree/dev/data/eval_videos) gespeichert. Auf dem Plot kann man sehen das der Agent bei 10 Runden im Schnitt einen positiven Reward erzielt, also die Spiele meistens gewinnt.

![eval_plot1](https://github.com/alexx1374/RL/assets/104265677/18d5fd5f-b86a-4f74-93cf-8db5bc69e1b1)


Durchschnittlicher Reward über 10 Episoden: 4.4

### Referenzen
Deep Q-Learning mit TensorFlow und Keras
OpenAI Gym-Dokumentation
