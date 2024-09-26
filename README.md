\# PMDM  
\#1.Anàlisi de l'estructura del projecte  
\-Comenta el tipus de projecte, quina estructura té (pots incloure captures de pantalla), i quins són els fitxers i carpetes més importants.  
Aquest projecte és del tipus aplicació Android.  
1.Descriptor de l'aplicació.  
2.Códi font de l'aplicació.  
3.Recursos.  
4.Scripts Gradle.  
![estructura](https://github.com/user-attachments/assets/5aa92cbc-da4e-4ae3-bc5d-eb1676a74b88)

1.Códi font de l'aplicació.  
2.Recursos.  
3.Descriptor de l'aplicació.  
4.Script Gradle per al projecte.  
5.Script Gradle per als mòduls.  
![estructura2](https://github.com/user-attachments/assets/1dd0a774-fa8a-4efb-a02b-0e349d78d8c2)


* Els scripts Gradle de construcció del projecte, en format Kotlin DSL (build.gradle.kts), tant el general, situat en l'arrel, amb informació comuna a tots els mòduls, com el propi del mòdul de l'aplicació (app/build.gradle.kts). En la vista d'Android, es mostren tots dos scripts dins de , indicant si és l'script corresponent al projecte o al mòdul.

* Dins de la carpeta del mòdul (app) trobem la carpeta src, que conté els el codi font de l'aplicació (app/src/main). En la vista Android, aquest es troba en la carpeta kotlin+java, i com veiem, es mostra en format de nom de paquet, en lloc de mostrar l'estructura de directoris.

* La carpeta app/src/res, que contindrà els recursos de l'aplicació (imatges, dissenys, cadenes de text, etc). Si ens fixem en el detall, aquesta carpeta conté bastants subcarpetas, per als diferents tipus de recursos. En la vista d'Android, es mostra aquest contingut de forma més compacta i organitzada , segons el tipus de recurs.

* El fitxer descriptor de l'aplicació: app/AndroidManifest.xml, amb informació associada a aquesta. Com veurem, es tracta d'un dels fitxers més importants del nostre projecte, ja que defineix aspectes com el nom de l'aplicació i el paquet, la icona, i els seus diferents components.

\-Si volguera afegir una nova activitat, sería suficient crear el fitxer de layout i el fitxer Kotlin amb la classe?  
No, crear només l'arxiu de layout i la classe Kotlin no és suficient per a afegir una nova activitat en Android Studio. Encara que estos són components essencials, hi ha altres aspectes que has de considerar perquè la nova activitat funcione correctament.

Crear la classe de l'activitat:  
Utilitza l'assistent d'Android Studio per a generar la classe de l'activitat. Això assegurarà que s'incloguen tots els mètodes i atributs necessaris.  
Definix el layout que s'associarà a esta activitat en l'atribut setContentView().

Crear el layout:  
Dissenya la interfície d'usuari de l'activitat utilitzant XML en l'arxiu de layout corresponent.

Registrar l'activitat en el manifest:  
Obri l'arxiu AndroidManifest.xml i agrega una nova etiqueta \<activity\> per a registrar l'activitat. Això li indica al sistema que existix una nova activitat en la teua aplicació.  
Especifica el nom de la classe de l'activitat i altres atributs com el tema, les intencions, etc.

Iniciar l'activitat des d'una altra part de la teua aplicació:  
Utilitza un Intent per a iniciar la nova activitat des d'una altra activitat, un servici o un fragment.

\#2.Análisi del clicle de vida i el problema de la pèrdua d'estat  
Al girar la pantalla passa pels cicles de vida de onPause, onStop, onDestroy, onCreate, onStart, onResume. La informació com podem observar la destruïm i la tornem a recrear.  
![estados](https://github.com/user-attachments/assets/a1d45ce2-e8f3-4775-90fc-66961c36b0bf)


\#3.Solució a la pèrdua d'estat  
Guardem el valor del comptador.  
![guardarvalor](https://github.com/user-attachments/assets/29e3c12d-50dd-4420-824b-4bb67c55fd37)
 
Restaurem el valor del comptador i actualitzem el TextView.  
![restaurarvalor](https://github.com/user-attachments/assets/7859738a-9397-4268-a68a-9316e8644014)


\#4.Ampliant la funcionalitat amb decrements i Reset  
Agregem les referències als botons  
![referenciaboton](https://github.com/user-attachments/assets/57d282be-e66c-4d22-993c-3f367ae19545)

Agregem la funcionalitat al fer click  
![respostaclick](https://github.com/user-attachments/assets/4efffbb1-d716-4c44-8d7a-2b85447f232b)


Eliminem esta línia del activity\_main.xml per a arreglar l'error de compilació  
![liniaerror](https://github.com/user-attachments/assets/f7ed977e-39d9-43d4-bc16-5ebf553a7579)


\#5.Canvis per implementar el View Binding

![buildfuture](https://github.com/user-attachments/assets/f386cc73-a4fa-4df4-8c8c-d8b71a95852f)
![canvi1](https://github.com/user-attachments/assets/5626c3e0-1658-4e41-991b-8e1c2a5ca490)
![canvi2](https://github.com/user-attachments/assets/c503eeb2-8d36-498e-b981-efdd24430007)
![canvi3](https://github.com/user-attachments/assets/a1b41789-737e-4768-9789-03d7c5d6b923)
