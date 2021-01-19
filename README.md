# ExoPattern
Exercice sur les patterns sur ue4 4.24

Tous les blueprints créés se trouvent dans content/ThirdPersonCPP/Blueprints.
Le level blueprint à lui aussi été modifié.

1 Stratégie pattern :
  Dans le blueprint "ThirdPersonCharacter" la fonction ("ShootWhat") s'adapte selon la variable "Element",
  faisant appel à une fonction("ShootFire") tirant une boule de feu si elle est égale à "Fire" ou 
  faisant appel à une fonction ("ShootElectricity") tirant une boulde de foudre si elle est égale à "Electricity".
  
2 Observer pattern :
 Sur les quatres bords extérieurs de la map se trouve des tores lumineux, de couleur orange quand la variable "Element" du
 "ThirdPersonCharacter" est "Fire" et de couleur bleu pour "Electricity". Le level blueprint possède un event tick qui
 surveille la variable Element, en cas de changement le level blueprint notifie les tores dont le nom de blueprint est 
 "BP_COLOR_WALL_OBSERVER"
 
 3 Command pattern :
  L'action mapping "interact" associé à la touche trace une ligne en cas de colision avec un objet. Si l'objet en question possède 
  une "Interaction Interface", alors une fonciton particulière selon l'objet est invoqué. Les pilliers permettent de changer d'élément,
  et la radio joue ou arrête la musique.
 
