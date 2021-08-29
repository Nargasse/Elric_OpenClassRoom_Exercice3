# Optimisation d'un site web

Cet exercice réalisé dans le cadre de mon parcours Open Class Room consistait à reprendre un site web existant et à en analyser les problèmes, notamment les soucis d'accessibilités, de SEO et d'optimisation, avant d'en publier un rapport d'analyse, puis de proposer une version du site résolvant 10 des problèmes relevés.

La première version du site est disponible dans la branche Main du dépôt, la version corrigé est disponible dans la branche "Changements", ainsi que le rapport complet d'analyse avec comparaison points par points. Notons que j'ai choisis de corriger non pas 10 mais 15 des points que j'ai relevé, certains équivalent à des changements très mineurs et facile à faire. J'ai en revanche laissé de côté principalement des points nécessitant un plus grand travail de mise à jour des outils du site, ou une discussion préalable avec le client pour s'assurer de la direction à prendre.

Voici la liste des changements que j'ai appliqués:
 1 : J'ai changé l'attribut langue de la balise HTML,
 2 : J'ai remplie la balise description, qui est souvent utilisé par les moteurs de recherche et dont ils recommandent la présence.
 3 : J'ai remplie la balise title.
 4 : J'ai changé une partie des "div" du site, de manière à employer quelques balises plus sémantiquement adapté, ce qui permet non seulement une meilleure accessibilité mais aussi un meilleur classement SEO.
 5 : J'ai enlevé certaines divisions cachés ne servant qu'à contenir des listes de mots-clés cachés. Cette pratique est fortement punie par les moteurs de recherches et va à l'encontre des normes W3C.
 6 : J'ai rajouté des attributs alt sur les images et les ai remplies avec une description de l'image en conformité avec les normes W3C et les recommendations ARIA.
 7 : J'ai ajouté quelques landmarks ARIA de manière à faciliter la navigation sur les navigateurs alternatifs.
 8 : J'ai transformé toutes les images présentant du texte en texte simple, ce qui permet de mieux gérer le responsive et enlève une grande partie d'images inutiles.
 9 : J'ai changé certains éléments de manières à créer un meilleur contraste entre les textes et leur fond, de manière à atteindre au moins les minimum ARIA.
 10 : J'ai changé le format des images à des formats plus optimaux et employé des outils pour les compressés avec un impact minimum sur la qualité.
 11 : J'ai aussi rendu une partie des images disponibles en webp, avec une balise picture permettant de fournir une image dans un format plus ancien en cas de besoin.
 12 : J'ai enlevé du footer tous les liens non cohérents avec le contexte du site, notamment tous les partenaires ou même annuaires présentés dedans. Ce genre de groupement de liens de tous genre est fortement pénalisé par les moteurs de recherches qui peuvent y voir une ferme de liens.
 13 : J'ai ajouté un effet visuel lorsqu'un élément reçoit le focus. Sans cela, un utilisateur naviguant au clavier ne peut pas savoir ce qu'il est en train de sélectionner sur une page. La plupart des navigateurs alternatifs reproduisant une navigation au clavier, c'est un critère majeur d'accessibilité.
 14 : J'ai changé légèrement la hiérarchie des titres de façons à respecter un ordre plus strict. Les titres sont souvent employés par certains navigateurs pour structurer la page, et il est important de bien respecter les normes W3C sur ce sujet.
 15 : J'ai marqué les fonts employés comme des images comme telle. Certaines personnes vont vouloir désactiver les fonts spéciales qui troubleraient leur lecture, il est alors important que les fonts qui ont un sens visuel particulier soit marqué pour rester visible lors de la lecture.

Voici la liste des changements que j'ai juste suggérés :
 * : J'ai suggéré des changements sur mots de la balise keywords. L'efficacité de cette balise est très discutable et il est probable que google n'en tienne pas du tout compte. Néanmoins, un trop plein de mots, surtout s'ils sont mal choisis pour le site, peut éventuellement contribué faire passer ça pour une tentative d'abus.
 * : J'aurais voulu révisé la feuille de style css, mais celle-ci s'appuyant lourdement sur une vieille version de bootstrap, des changements à ce niveau la m'aurait nécessité une grosse quantité de travail et une discussion avec le client pour orienter les changements d'une manière qui lui convienne. J'ai donc choisis de laisser les feuilles de styles de côtés, ne les modifiants que de façon minimal pour corriger certains problèmes du site.
 * : J'ai remarqué que certains liens vers des scripts js et css n'étaient employés nul part sur le site, notamment par exemple un link vers l'api google map. Néanmoins, n'étant pas sûr des raisons du clients pour les laissés la, j'ai décidé de ne pas y toucher pour le moment.
 * : J'ai remarqué qu'une grosse partie du temps de chargement de la page était dû aux fichiers javascript. Une grande partie des fonctionnalités auraient probablement pu être implémentés directement dans le html et le css, une autre partie aurait pu être retardé pour après le chargement. Une autre partie aurait probablement pu être simplement supprimé. Néanmoins, cela représente une quantité conséquente de travail dont il aurait fallu discuter avec le client, j'ai donc laissé cette partie de côté.
 * : J'ai remarqué la présences de liens invisibles et inutilisables, dû à un dysfonctionnement de l'un des scripts, des contradictions de règles CSS et des classes mal attribués suite à une dé-minification du site.
 * J'ai remarqué la présences d'une très grande quantité de classes CSS dont une partie inutilisés. Il serait utile d'en faire un audit pour en minimiser la quantité.
 * J'ai remarqué que les textes étaient mesurés en px plutôt qu'en em, ou autres mesures dynamiques plus pratique. Notons que les dernières versions de Bootstrap comptent en em plutôt qu'en px, et qu'une mise à jour du framework solutionnerais donc le problème.
 * J'ai noté que les titres de pages et les noms de certains liens étaient extrêmement peu clair, ce qui peut rendre un utilisateur confus et rendre le site moins lisible pour les robots.
