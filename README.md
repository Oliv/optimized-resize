# jquery.optimizedResize 1.0.1
jquery.optimizedResize
===========

Optimisation de l'évènement resize
Inspiré de MDN <https://developer.mozilla.org/>

Prérequis
----------

Inclure jQuery
Copier le répertoire du script dans js du projet

Inclure le script

    <script src="js/optimized-resize/jquery.optimizedResize.js"></script>


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

    <script>
        (function($) {
            $(document).ready(function() {
                $.optimizedResize.add(function() {
                    console.log('trigger à chaque resize');
                });
            });
        })(jQuery);
    </script>
