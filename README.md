# Python-cours



---

## **Découverte du BAC Pro CIEL (5 min)**

### **Qu’est-ce que le BAC Pro CIEL ?**

Le **BAC Pro CIEL** signifie **Cybersécurité, Informatique et réseaux, Électronique**.  
C'est une formation qui permet de :

- ** réseaux informatiques** (Wi-Fi, Internet, etc.)
- **Programmer des systèmes électroniques**, comme des objets connectés, des robots, ou des cartes électroniques ( Raspberry Pi !)
- **Protéger les systèmes informatiques** contre les cyberattaques (cybersécurité)

### **Pourquoi c’est passionnant ?**

- Tu peux **programmer** des objets pour qu'ils fassent exactement ce que tu veux (robots, lumières, alarmes, etc.).
- Tu comprends comment fonctionne le monde numérique autour de toi : Internet, smartphones, jeux vidéo, etc.
- C'est un secteur avec **beaucoup de débouchés** : technicien réseau, développeur, spécialiste en cybersécurité, etc.

---

## **Défi : "Le Défi de la LED Magique" (20 min)**

### **Objectifs :**

- Découvrir les bases de Python
- Programmer une LED avec un Raspberry Pi
- Comprendre le lien entre le code et le matériel

---

### **Déroulement de l’activité**

### 🔴 **Défi 1 : Allumer la LED (5 min)**

**Consigne :** Écris un programme Python pour allumer la LED.

```python
from gpiozero import LED

led = LED(21)  # La LED est connectée au GPIO 17
led.on()       # Allumer la LED
```

- **Question bonus :** Que fait le code si tu remplaces `led.on()` par `led.off()` ?

---

### ⚡ **Défi 2 : Faire Clignoter la LED (10 min)**

**Consigne :** Fais clignoter la LED toutes les secondes.

```python
from gpiozero import LED
from time import sleep

led = LED(21)

while True:
    led.on()
    sleep(1)   # Attendre 1 seconde
    led.off()
    sleep(1)
```

- **Challenge bonus :** Modifie la vitesse du clignotement (change la valeur de `sleep()`).
- **Idée :** Essaie avec `0.2` pour un clignotement rapide.

---

### 🚀 **Super Défi : Le Code Secret (5 min)**

**Consigne :** Crée un code lumineux : 3 clignotements rapides suivis d'une longue pause (comme un signal de détresse en morse).

```python
from gpiozero import LED
from time import sleep

led = LED(21)

while True:
    for _ in range(3):  # 3 clignotements rapides
        led.on()
        sleep(0.2)
        led.off()
        sleep(0.2)
    sleep(2)  # Pause longue
```

---

### **Conclusion (5 min)**

- **Ai-je bien compris :**
    - Qu’est-ce qu’une boucle `while True` ?
    - Comment fait-on pour ralentir ou accélérer le clignotement ?
    - Que se passe-t-il si on change le chiffre `3` dans le dernier code ?

---



"En BAC Pro CIEL, vous ferez ce genre de projets, mais avec des systèmes de plus en plus complexes : des réseaux, des robots, de la cybersécurité… et beaucoup d’expérimentations comme aujourd’hui !"

---

### **Matériel**
- Raspberry Pi 400 (un par groupe ou par élève)
- 1 LED Jaune par Raspberry Pi
- 1 résistance de 87 Ω
- Bread board
- Fils de connexion (le câblage est déjà fait par vous)

---

