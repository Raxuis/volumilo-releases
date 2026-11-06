# Bien démarrer avec Volumilo

[← Présentation](README.md) · [English](QUICKSTART.en.md)

## Installer Volumilo

Il faut un Mac **Apple Silicon** et **macOS 14 ou plus récent**. La version Intel n’est pas validée.

1. Ouvrez la [dernière version publiée](https://github.com/Raxuis/volumilo-releases/releases/latest) et téléchargez **Volumilo.dmg**. Aucun compte GitHub n’est nécessaire.
2. Ouvrez le DMG, puis glissez **Volumilo.app** vers **Applications**.
3. Éjectez le DMG et ouvrez la copie dans Applications.

La version actuelle porte une signature locale ad-hoc et n’est **pas notariée par Apple**. Les empreintes du DMG et du ZIP figurent dans `SHA256SUMS` sur la page de la version ; elles permettent de vérifier la correspondance du téléchargement, pas de remplacer la validation d’Apple.

### Si macOS bloque l’ouverture

Vérifiez d’abord que le téléchargement vient du dépôt officiel ci-dessus. Si vous décidez de faire confiance à cette version, après avoir tenté de l’ouvrir, consultez **Réglages Système → Confidentialité et sécurité** et l’option **Ouvrir quand même**, lorsqu’elle est disponible. Confirmez vous-même la demande de macOS. Les libellés peuvent varier selon sa version. [Procédure officielle Apple](https://support.apple.com/fr-fr/102445).

N’utilisez pas cette procédure si macOS signale un logiciel malveillant ou une app altérée/endommagée : arrêtez-vous et vérifiez le téléchargement. Volumilo ne demande pas de désactiver la sécurité globale du Mac.

## Choisir votre premier parcours

| Votre besoin | Où commencer | Ce qui se passe |
|---|---|---|
| Comprendre un disque plein | **Mon disque est presque plein** ou **Analyser un dossier…** | Vous lancez une analyse, puis explorez les tailles mesurées. |
| Comprendre une app volumineuse | **Applications…** | Vous choisissez une app, puis lancez son analyse ciblée. |
| Préparer une copie externe | **Déplacer vers un disque externe** ou menu **Transfert vérifié…** | Vous choisissez les sources et la destination ; ouvrir la fenêtre ne copie rien. |

## Explorer, puis sélectionner

Cliquez une fois sur un dossier dans **Contenu**, ou sur un secteur du graphique, pour l’explorer. Le centre du graphique et le bouton de dossier parent permettent de remonter. Le clic droit propose les actions disponibles.

Glissez les fichiers et dossiers à examiner dans **Sélection à vérifier**. Le dépôt ne déplace ni ne supprime les fichiers. Relisez la sélection et les avertissements avant de confirmer une action. Les suggestions peuvent inclure des caches utiles ou des fichiers à conserver : le choix vous appartient.

## Garder un catalogue hors ligne

1. Analysez le volume entier d’un disque externe ou d’une carte SD.
2. Dans le menu d’informations de l’analyse, choisissez **Enregistrer le catalogue du disque…**, puis relisez et confirmez la sauvegarde.
3. Ouvrez **Volumilo → Catalogues des disques…** et recherchez un nom, un fragment de chemin ou une extension.
4. Vous pouvez ensuite éjecter votre disque dans Finder. Le catalogue reste consultable, y compris après relance.

Le catalogue est une observation datée. La reconnexion ne le met pas à jour automatiquement. Pour le remplacer, effectuez une nouvelle analyse et confirmez un nouvel enregistrement. **Oublier ce catalogue** retire seulement les métadonnées locales, jamais les fichiers du disque.

L’ouverture d’un emplacement depuis l’historique exige de nouveaux contrôles d’identité. Elle est actuellement limitée à APFS/HFS ; sur FAT/exFAT, reconnectez et analysez le disque pour naviguer dans ses résultats actuels. La recherche historique reste disponible.

## Préparer un transfert vérifié

Ajoutez les fichiers ou dossiers sources, puis choisissez un dossier sur **un autre volume externe local et accessible en écriture**. Préparez le récapitulatif, vérifiez-le, puis lancez explicitement la copie et la vérification. La relecture prend du temps : il ne s’agit pas d’une simple copie.

Une fois la vérification terminée, examinez séparément les originaux. Leur mise à la Corbeille exige une confirmation supplémentaire et peut être bloquée si les fichiers ont changé ou si certaines métadonnées ne sont pas compatibles. Aucune suppression d’originaux n’est lancée automatiquement. Conservez vos sauvegardes habituelles.

Le journal permet une reprise volontaire après relance ou reconnexion. Il retient des chemins et l’avancement, sans contenu de fichier. Une reconnexion ambiguë ou un fichier modifié peut nécessiter une nouvelle préparation.

## À savoir

- **Autorisations** : macOS peut demander l’accès aux dossiers ou volumes que vous choisissez. Les refus et emplacements illisibles sont signalés ; une analyse partielle ne décrit pas tout le disque. Les réglages ne fournissent pas d’accès administrateur universel.
- **Tailles** : les analyses montrent l’espace alloué observé, qui peut différer de la taille logique et de l’espace réellement récupérable. Les blocs partagés, instantanés et emplacements non lus peuvent expliquer des écarts.
- **Corbeille** : y déplacer un fichier ne garantit pas un gain immédiat. Volumilo ne la vide pas automatiquement. Une option de suppression définitive existe séparément, avec confirmation et compte à rebours ; elle est irréversible.
- **Cloud** : la vue concerne les dossiers synchronisés du Finder. Elle n’inventorie pas tout un compte distant. Les outils de transfert et certains contrôles refusent les éléments non locaux ou cloud.
- **Conservation** : les analyses ordinaires disparaissent à la fermeture. Les catalogues enregistrés volontairement, les dossiers/seuils de surveillance et les journaux ont leurs propres règles de conservation ; les mesures de surveillance restent en mémoire.
- **Vérification de transfert** : elle concerne la copie contrôlée à ce moment, sans garantir l’état futur du support ni constituer un instantané atomique des sources.

## Mettre à jour

Ouvrez **Volumilo → Rechercher des mises à jour…**. L’app consulte le catalogue public et ouvre le téléchargement dans votre navigateur ; elle ne se remplace pas automatiquement. Quittez l’ancienne version avant de la remplacer dans Applications. Les analyses conservées uniquement en mémoire seront perdues.

Pour un problème, notez la version de l’app, celle de macOS, le type de volume et le message affiché. Évitez de partager des noms ou chemins privés dans les captures.
