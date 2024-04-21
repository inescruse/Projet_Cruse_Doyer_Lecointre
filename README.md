TITRE : SIMULATEUR DE CARNET D'ORDRES EN PYTHON

DESCRIPTION

Ce projet consiste en une simulation d'un carnet d'ordres pour les marchés financiers, permettant de gérer des ordres d'achat et de vente dans un environnement de trading électronique. Le simulateur offre des fonctionnalités pour ajouter, exécuter, et annuler des ordres, ainsi que simuler des fixings de prix d'ouverture et de fermeture. Cet outil est conçu pour aider les développeurs, les étudiants et les professionnels de la finance à comprendre la dynamique des carnets d'ordres et leur impact sur la détermination des prix sur les marchés.

INSTALLATION

Prérequis
Assurez-vous d'avoir Python installé sur votre machine (Python 3.6 ou plus récent est recommandé). Aucune dépendance externe n'est requise pour exécuter ce projet.

Téléchargement
Pour installer le simulateur de carnet d'ordres, clonez ce dépôt GitHub en utilisant la commande suivante : git clone [URL_DU_DEPOT_GITHUB]
Remplacez `[URL_DU_DEPOT_GITHUB]` par l'URL du dépôt de votre projet.

Configuration
Aucune configuration initiale n'est nécessaire pour commencer avec ce simulateur. Le projet est prêt à être utilisé dès que vous avez cloné le dépôt.

UTILISATION

Création d'une instance de `OrderBook`
Pour démarrer, créez une instance de la classe `OrderBook` en spécifiant la taille du tick et la taille du lot. Exemple : order_book = OrderBook(tick_size=0.01, lot_size=10)

Ajout d'ordres
Pour ajouter un ordre au carnet, utilisez la méthode `add_order` :
order_book.add_order('buy', 100.05, 100, 'participant1', 'maker')
order_book.add_order('sell', 101.05, 50, 'participant2', 'maker')

Exécution du fixing
Pour exécuter le fixing et déterminer le prix de marché :
fixing_price = order_book.fixing()
print(f"Prix de fixing : {fixing_price}")

Affichage du carnet d'ordres
Pour voir l'état actuel du carnet d'ordres :
order_book.print_order_book()

Affichage de l'historique des transactions
Pour consulter l'historique des transactions effectuées :
print("\nHistorique des transactions:")
for transaction in order_book.get_transaction_history():
    print(transaction)

CONTRIBUTIONS

Clonage du dépôt
Pour contribuer au projet, commencez par cloner le dépôt :
git clone [URL_DU_DEPOT_GITHUB]

Soumission de contributions
Après avoir apporté vos modifications ou améliorations, soumettez une pull request via GitHub. Assurez-vous de décrire clairement les changements proposés et leur raison.

Signalement de problèmes
Si vous rencontrez des problèmes ou des bugs, n'hésitez pas à ouvrir un issue sur le dépôt GitHub du projet avec une description détaillée du problème et, si possible, des étapes pour reproduire le problème.

CONCLUSION

Ce simulateur de carnet d'ordres est un projet open-source et les contributions pour améliorer ou étendre ses fonctionnalités sont toujours les bienvenues. Ce simulateur est destiné à être utilisé comme outil pédagogique et de développement pour mieux comprendre le fonctionnement des marchés financiers.
