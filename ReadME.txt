
---------------------------------------------------------------------
Visualisateur de trafic réseau (2022-2023)                           |
                                                                     |
Projet de IDJER Samy Remy  21208501 et Mussard Wassim 28706762       |
Réseaux LU3IN033 Groupe 2                                            |
                                                                     |
---------------------------------------------------------------------    
                                                                
Main.py:

Dans ce fichier principal, on retrouvera les fonctions liées au décodage d'un paquet, en analysant tous les champs  de la couche Ethernet à la couche Application : 

HexToDec(liste: valeurs Hexadecimal) -> Liste de valeurs où chaque  valeurs est converti  en décimal.
HexSumtoDec(liste: valeurs Hexadecimal) -> Somme chaque valeurs de la liste  converti en decimal.
HexToType(protocol: valeur Hexadecimal ) -> Renvoie le type du protocol associé au code héxadécimal.

DestAddIP, SrcAddIP, DestAddMAC, SrcAddMAC, SrcAddMAC, DestPort, commentaire, type -> Liste avec l'attribut en question de chaque trame analysée.
ethernet(i), ip(i), icmp(i), arp(i), tcp(i), udp(i) , http(i) -> Analyse de l'entète en question de la trame "i".
trameTotal(i) -> Analyse toutes les entètes  de la trame "i".

output() -> Créer dans le répertroire courrant un fichier "output.txt" où on va retrouver le résultat du visualisateur. Si le fichier existe déja, il sera alors remplacé.

Interface.py : 

Dans ce fichier secondaire , on retrouvera donc principalement les fonctions liée à l'interface  :

start(liste : srciP, liste : dstiP, liste : protocol, liste : destMac, liste : srcMac, liste: srcPort, liste : dstPort, liste : times, liste : comment) -> Prend en paramètre une liste pour chaque champs liés à l'interface et va lancer la fonction  "interface".
interface(liste : srciP, liste : dstiP, liste : protocol, liste : destMac, liste : srcMac, liste: srcPort, liste : dstPort, liste : times, liste : comment) -> La fonction va initialisée l'interface en utilisant  la bibliothèque "Tkinter". 
init(interface(liste : srciP, liste : dstiP, liste : protocol, liste : destMac, liste : srcMac, liste: srcPort, liste : dstPort, liste : times, liste : comment) -> initialise le contenue de la fenêtre, ajout des adresses iP et Mac , des ports, le temps et les commentaires . 
affichePort(entier : i,liste : dico_ip,liste : srciP, liste : dstiP,liste : srcPort,liste : dstPort, entier : p) -> Affiche les ports dans la fenêtre.
v_scroll(*args) -> Fonction permettant de synchroniser plusieurs fenêtres avec une "scrollbar".
filtre(event) -> Fonction , qui en fonction du filtre choisit par l'utilisateur, va mettre à jour l'interface.
