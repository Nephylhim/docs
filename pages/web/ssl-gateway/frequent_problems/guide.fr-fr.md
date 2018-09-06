---
title: Problèmes fréquents
slug: problemes-frequents
excerpt: Des réponses face à quelques problèmes fréquents
section: Utilisation
---

## Problèmes fréquents

> [!faq]
>
> J'ai un hébergement web et je n'arrive pas à commander de SSLGateway
>> L'offre d'hébergement web propose déjà une option https. Vous trouverez de plus amples informations ici : ![Les certificats SSL sur les hebergements web](https://docs.ovh.com/fr/hosting/les-certificats-ssl-sur-les-hebergements-web/)
>
> L'ajout de mon domaine est long
>> Afin de pouvoir valider le challenge Let's Encrypt, votre nom de domaine doit pointer sur la SSLGateway. Une modification DNS peut prendre jusqu'à 48h (cela prend généralement moins de temps). Une fois le domaine correctement routé, nous procédons à la demande du certificat et le délivrons au plus vite.
>
> J'ai une erreur 503 quand je requête mon site
>> Plusieurs cas peuvent conduire à des erreurs 503 :
>>> - Vous avez activé la "redirection https" alors que votre certificat n'est pas encore délivré. Cette option permet de rediriger automatiquement les utilisateurs vers la version https de votre site (http -> https). Cette option est déconseillée tant que le https n'est pas fonctionnel.
>>> - Vous avez activé "serveur https" mais votre serveur ne gère pas celui-ci. Cette option signifie que votre serveur gère l'https et que la SSLGateway enverra les requêtes clientes à votre serveur en https.
>>> - Vous avez une boucle de redirection. Par exemple, votre serveur redirige la requête sur le nom de domaine lorsqu'il est requêté par son adresse ip. Cela créé une boucle de redirection puisque la SSLGateway envera la requête sur l'adresse ip de votre serveur qui redirigera vers la SSLGateway.
>
> Mon site est cassé / Je peux requêter mon site en https mais le navigateur m'indique que la connexion n'est pas sécurisée.
>> Vous avez peut-être du contenu mixte sur votre site (mixed content en anglais). Mozilla propose un très bon guide pour ![régler le problème du contenu mixte dans un site web](https://developer.mozilla.org/fr/docs/S%C3%A9curit%C3%A9/MixedContent/regler_probleme_contenu_mixte_site_web)
>
> J'ai supprimé ma SSLGateway mais je ne peux pas en commander un autre.
>> Une seule SSLGateway peut-être délivré pour un nom de domaine donné. Ainsi, une SSL Gateway pour laquelle une demande de fin de service à été demandée, reste suspendue jusqu’à la date d'expiration originale, empêchant alors de réutiliser le domaine associé. Une fois cette date d'expiration atteinte, votre SSLGateway sera supprimée et vous pourrez à nouveau en commander une.
>
> J'ai une websocket sur mon site et je me fais déconnecter au bout de 10 minutes.
>> Le produit SSLGateway possède effectivement un timeout de 10 minutes. Ce paramètre est non modifiable.

## Outils

Quelques outils peuvent vous aider à diagnostiquer vos problèmes :

- ![Why No Padlock](https://www.whynopadlock.com/) : Cet outil peut vous aider à trouver ce qu'il manque à votre site pour fonctionner correctement en https.
- ![Test DNS](https://testdns.fr/) : Cet outil vous permet de vérifier la configuration DNS de votre nom de domaine.

## Vous n'avez pas trouvé de solution à votre problème ?

Vous pouvez présenter votre problème sur le ![forum communautaire OVH Community dédié au produit SSLGateway](https://community.ovh.com/c/web-hosting/ssl-gateway). D'autres utilisateurs ainsi que du personnel OVH tenteront de vous aider à résoudre votre problème.
