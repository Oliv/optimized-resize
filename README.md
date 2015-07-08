# jquery.optimizedResize 1.0.1
jquery.optimizedResize
===========

Optimisation de l'évènement resize
Inspiré de MDN <https://developer.mozilla.org/>

Prérequis
----------

Copier le répertoire du script dans js du projet

Inclure le script (soit dans include/fo.entete.php et include/pseudo.entete.php, soit dans le fichier php voulu)

    CMS::addJS(SERVER_ROOT . 'include/js/jquery.optimizedResize/1.0.1/jquery.optimizedResize.js');


Utilisation
----------

Le script est un objet global jquery, accessible par

    $.optimizedResize

Il expose la méthode suivante :


### Add : #

    $.optimizedResize.add(callback)

callback : une fonction qui sera jouée à chaque resize, en prenant en compte l'utilisation mémoire et le fps


Application
----------

    $(document).ready(function() {
        $.optimizedResize.add(function(i18n) {
            ...

            console.log('trigger à chaque resize');
        });
    });
