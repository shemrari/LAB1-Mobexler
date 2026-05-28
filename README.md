LAB 1 : Mise en place de l’environnement de test (Mobexler + snapshot propre)
Étape 1 : Vérification du téléchargement de Mobexler

Avant l’importation, l’intégrité du fichier OVA a été contrôlée.
Le hash SHA256 du fichier local a été généré à l’aide de la commande :
Get-FileHash .\Mobexler.ova -Algorithm SHA256

Ce hash a ensuite été comparé à celui fourni sur le site officiel de Mobexler.

 <p align="center"> <img src="images/img3.png" width="500"> </p>

Les deux empreintes étant identiques, le fichier est complet et non corrompu.

Étape 2 : Importation de Mobexler dans VirtualBox

La machine virtuelle a été importée dans VirtualBox avec succès.

 </p> <p align="center"> <img src="images/img5.png" width="800"> </p>

Après importation, la configuration réseau a été ajustée dans les paramètres de la VM :

<p align="center"> <img src="images/img6.png" width="800"> </p> <p align="center"> <img src="images/img20.png" width="800"> </p>
Étape 3 : Démarrage de la machine et accès initial

La machine virtuelle a été démarrée pour la première fois afin de vérifier son bon fonctionnement.

<p align="center"> <img src="images/img1.png" width="700"> </p>

Accès au terminal de la machine :

<p align="center"> <img src="images/img8.png" width="700"> </p>
Étape 4 : Vérification de la configuration réseau
Affichage des interfaces réseau avec la commande ip a :
<p align="center"> <img src="images/img9.png" width="700"> </p>
enp0s17 : 10.0.2.15/24 → NAT (accès Internet via VirtualBox) <p align="center"> <img src="images/img10.png" width="700"> </p>
enp0s8 : 192.168.56.103/24 → Host-Only (communication entre la VM et l’hôte) <p align="center"> <img src="images/img11.png" width="700"> </p>
Vérification des routes réseau avec ip route :
<p align="center"> <img src="images/img12.png" width="700"> </p>
Test de connectivité Internet :
<p align="center"> <img src="images/img13.png" width="700"> </p> <p align="center"> <img src="images/img14.png" width="700"> </p>
Étape 5 : Création d’un snapshot

Un snapshot a été créé afin de conserver un état propre de la machine virtuelle avant les tests.

<p align="center"> <img src="images/img15.png" width="700"> </p> <p align="center"> <img src="images/img16.png" width="800"> </p>
Étape 6 : Mise en place de l’environnement Android pour les tests
Activation du mode développeur sur le téléphone (7 appuis sur le numéro de build)
<p align="center"> <img src="images/mobile2.jpeg" width="350"> </p>
Activation du débogage USB dans les options développeur
<p align="center"> <img src="images/mobile1.jpeg" width="350"> </p>
Connexion du téléphone à la VM via VirtualBox (USB)
Dans les paramètres de la machine virtuelle, ajout du périphérique USB correspondant au téléphone :
<p align="center"> <img src="images/img19.png"> </p>
Vérification d’ADB dans Mobexler :
<p align="center"> <img src="images/img18.png"> </p> <p align="center"> <img src="images/img17.png"> </p>