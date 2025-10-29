**ANY OTHER DECK NOT MENTIONED ON THIS PAGE IS NOT AFFILIATED WITH ME, INCLUDING ANY AI OR PAID MODIFICATIONS.**

# Kaishi 1.5k

Bienvenue sur le répertoire public pour **Kaishi 1.5k**, un deck Anki moderne créé pour permettre aux débutants d'apprendre les bases du vocabulaire japonais. Kaishi 1.5k est hautement modulaire, et cette page est dédiée à vous enseigner les différentes options que vous pouvez modifier pour ajuster le deck selon vos préférences. Voici à quoi ressemble la face avant d'une carte :

<img src="https://github.com/donkuri/Kaishi/blob/main/pics/kaishi-front.png" alt="Front of a Card in Kaishi 1.5k" style="width: 100%; height: auto">

Comme vous pouvez le voir, on y trouve le mot et la phase, dans laquelle le mot est mis en avant, ce qui permet de le distinguer plus rapidement. Une fois que le mot est bien connu, il est bien plus facile de le réviser, puisque le mot apparaît en premier. Voici à quoi ressemble la face arrière de la carte sur le deck par défaut :

<img src="https://github.com/donkuri/Kaishi/blob/main/pics/kaishi-back.png" alt="Back of a Card in Kaishi 1.5k" style="width: 100%; height: auto">

Contrairement aux autres decks de type Core, on découvre la lecture du mot avec les furiganas avant de voir sa signification. L'audio, ainsi que la phrase sont ensuite disponibles. Rendez-vous plus bas pour découvrir comment ajouter les hauteurs d'accent. S'il existe des notes pour cette carte, elles sont affichés juste en-dessous. 

[Si vous êtes débutant·es en Japonais ou en immersion, lisez ce guide dans un premier temps.](https://donkuri.github.io/learn-japanese/fr/guide/)

### Sommaire

- [Comment télécharger le deck ?](#comment-t%C3%A9l%C3%A9charger-le-deck-)
- [Comment utiliser ce deck ?](#comment-utiliser-ce-deck-)
- [Autres decks en lien](#autres-decks-en-lien)
- [Quelles options sont disponibles pour ce deck ?](#quelles-options-sont-disponibles-pour-ce-deck-)
- [L'audio ne correspond pas au mot !](#laudio-ne-correspond-pas-aux-mots-)
- [Je n'aime pas les images !](#je-naime-pas-les-images-)
- [Comment importer Kaishi dans un autre deck](#comment-importer-kaishi-dans-un-autre-deck)
- [La genèse du deck](#la-genèse-du-deck)
- [Traduction du deck](#traduction-du-deck)
- [Que faire après ce deck ?](#que-faire-après-ce-deck-)
- [Crédits](#crédits)

## Comment télécharger le deck ?

Vous pouvez soit télécharger le deck sur la page [releases](https://github.com/donkuri/Kaishi/releases/) de ce GitHub ou sur AnkiWeb [AnkiWeb](https://ankiweb.net/shared/info/1196762551), si le deck n'est pas en cours de révision. **Ce deck fonctionne sur Anki 2.1.50+.**

## Comment utiliser ce deck ?

Pour une explication sur la façon dont Kaishi s'intègre avec l'apprentissage du Japonais de manière générale, consultez ce [guide](https://donkuri.github.io/learn-japanese/fr/guide/).

## Autres decks en lien

ねむい a créé un deck pour les radicaux basé sur celui de Kaishi 1.5k, reliant tous les radicaux avec leur première occurrence dans Kaishi. Il couvre aussi quelques radicaux supplémentaires qui ne sont pas dans Kaishi. Vous pouvez **utiliser ce deck en parallèle avec Kaishi si vous avez des difficultés avec les kanjis**, puisqu'il introduit les radicaux de kanjis au fur et à mesure, pour vous aider à mieux les lire. Vous pouvez trouver le deck [here on AnkiWeb](https://ankiweb.net/shared/info/1722008986). Merci ねむい !

## Quelles options sont disponibles pour ce deck ?

Il existe différentes options pour personnaliser vos cartes. Pour les modifier, sélectionnez le deck Kaishi, cliquez sur `Parcourir`, sélectionnez n'importe quelle carte du deck, puis cliquez sur `Cartes...` en haut à droite de la fenêtre.

### Hauteurs d'accent

L'option la plus importante est que vous pouvez choisir d'inclure ou non les hauteurs d'accents sur vos cartes. Actuellement, que l'on doive apprendre ou non les hauteurs d'accent soulève encore des débats houleux dans la communauté. Nous avons choisi de laissez le choix à l'apprenant·e, vous pouvez anisi choisir de l'intégrer à votre apprentissage si vous le souhaitez. Si vous choisissez de ne pas activer l'option, vous pourrez toujours le faire plus tard. Activer les hauteurs d'accent est facile.  L'option se trouve dans les options de cartes à l'onglet `Modèle du verso` (cliquez sur le petit point).

```CSS
<div lang="ja">
{{furigana:Word Furigana}}

<!-- This part enables pitch accent.

{{#Pitch Accent}}
	<br><div style='font-size: 24px'>{{Pitch Accent}}</div>
{{/Pitch Accent}} 

-->

<div style='font-size: 25px; padding-bottom:20px'>{{Word Meaning}}</div>
<div style='font-size: 25px;'>{{furigana:Sentence Furigana}}</div>
<div style='font-size: 25px; padding-bottom:10px'>{{Sentence Meaning}}</div>

{{Word Audio}}
{{Sentence Audio}}
<br>
{{Picture}}

{{#Notes}}
	<br>
	<div style="font-size: 20px; padding-top:12px">Note: {{Notes}}</div>
{{/Notes}}

<!-- This part enables pitch accent notes.

{{#Pitch Accent Notes}}
<div style="font-size: 20px; width: fit-content; max-width:40vw; margin: auto">
	<details><summary>Pitch Accent Notes</summary>
		<br>{{Pitch Accent Notes}}
	</details>
</div>
{{/Pitch Accent Notes}}

-->

</div>
```

Pour activer les hauteurs d'accent, vous devez simplement effacer tous les `<!--` et `-->`, pour obtenir le résultat suivant : 

```CSS
<div lang="ja">
{{furigana:Word Furigana}}

{{#Pitch Accent}}
	<br><div style='font-size: 24px'>{{Pitch Accent}}</div>
{{/Pitch Accent}} 

<div style='font-size: 25px; padding-bottom:20px'>{{Word Meaning}}</div>
<div style='font-size: 25px;'>{{furigana:Sentence Furigana}}</div>
<div style='font-size: 25px; padding-bottom:10px'>{{Sentence Meaning}}</div>

{{Word Audio}}
{{Sentence Audio}}
<br>
{{Picture}}

{{#Notes}}
	<br>
	<div style="font-size: 20px; padding-top:12px">Note: {{Notes}}</div>
{{/Notes}}

{{#Pitch Accent Notes}}
<div style="font-size: 20px; width: fit-content; max-width:40vw; margin: auto">
	<details><summary>Pitch Accent Notes</summary>
		<br>{{Pitch Accent Notes}}
	</details>
</div>
{{/Pitch Accent Notes}}

</div>
```

**Pour voir comment fonctionnent les hauteurs d'accent, consultez [cet issue](https://github.com/donkuri/Kaishi/issues/104#issuecomment-3171889366)**. (lien en anglais)

### Options secondaires

Il existe quelques autres options que vous pouvez modifier.

#### Furigana
Si vous voulez retirer les furiganas, enlevez simplement les parties `furigana:` du modèle de verso.

#### Autres options

Vous pourriez complètement changer le type de cartes que vous voulez voir. Ci-dessous, le `Modèle du recto` de Kaishi 1.5k:

```CSS
<div lang="ja">
{{Word}}
<div style='font-size: 20px;'>{{Sentence}}</div>
</div>
```

Comme vous pouvez le voir, nous avons seulement le mot et la phrase. Si vous voulez des cartes contenantant seulement la *phrase*, retirez la partie `{{Word}}`, ou mettez `Sentence` à l'intérieur et enlevez le reste. Si vous voulez des cartes contenat uniquement les *mots*, retirez simplement la partie `<div style='font-size: 20px;'>{{Sentence}}</div>`. Si au contraire vous voulez des cartes *audio*, retirez tout et ajoutez `{{Word Audio}}`, `{{Sentence Audio}}` ou les deux si vous le souhaitez.

#### Changer les fontes, tailles de police et autres options de style

Voici le modèle de `Styling` de Kaishi 1.5k:

```CSS
.card {
 font-family: "ヒラギノ角ゴ Pro W3", "Hiragino Kaku Gothic Pro", "Noto Sans JP", Osaka, "メイリオ", Meiryo, "ＭＳ Ｐゴシック", "MS PGothic", "MS UI Gothic", sans-serif;
 font-size: 44px;
 text-align: center;
}

img {
max-width: 300px;
max-height: 250px;
}

.mobile img {
max-width: 50vw;
}

/* Cette partie définit la couleur des mots en gras. */
b{color: #5586cd}
```

Vous pouvez trouver les différentes options de style [ici](https://docs.ankiweb.net/templates/styling.html). Comme vous pouvez le oir, kaishi 1.5k utilise très peu d'options dans l'onglet Styles. Vous pouvez changer l'option `font-family` si vous souhaitez utiliser une autre typographie, `font-size` pour changer la taille de la fonte et `text-align` pour modifier l'alignement du texte, si vous souhaitez que le texte soit aligné à gauche par exemple. Par défaut, Kaishi 1.5k colore les mots en **gras**. L'option pour changer cela est `b{color: }`, comme vous pouvez le voir ci-dessus. Mettez simplement un code hexadécimal ou un nom de couleur en anglais comme `red` pour l'appliquer à la place. Si vous ne voulez aucune color, retirez cette ligne.

## L'audio ne correspond pas aux mots !

Certains mots comme 次 (つぎ) et あげる ont été reportés comme ayant un "mauvais" audio. C'est parce que souvent les débutant·es n'entendent pas (et ne connaissent pas) la nasalisation Japonaise, où le son du /g/ peut sembler plus proche du /n/. Regardez [cette vidéo](https://www.youtube.com/watch?v=xpzpbuFHVVU) pour comprendre comment cela fonctionne. **Malheureusement, un audio avec une forme non-nasalisée de ces mots est rarement disponible.**

## Comment importer Kaishi dans un autre deck

Si vous avez déjà commencé Core2k ou Tango N4-N5 (ou tout autre deck similaire) et que vous souhaitez passer à Kaishi 1.5k, vous pouvez suivre cette procédure, écrite par [Kuuube](https://github.com/Kuuuube).

**Attention : procédure non-testée avec la version française du deck de Kaishi 1.5k !**

1. Importez Kaishi normalement avec le fichier .apkg
2. Allez dans `Fichier > Exporter...` et exportez le deck Kaishi en utilisant `Notes en texte (.txt)`. Laissez tous les autres paramètres par défaut.
3. Supprimez le deck Kaishi.
4. Sélectionnez le deck dans lequel vous voulez importer Kaishi, sélectionnez `Parcourir`, cliquez sur n'importe quelle carte, appuyez sur `ctrl + a`, et sélectionnez `Notes > Modifier le type de la note...` dans le menu en haut de la fenêtre. Assurez-vous que toutes les notes que vous avez sélectionné sont du même type de notes, ou sinon `Notes > Modifier le type de la note...` risque de ne pas apparaître.
5. Changez le type de note pour `Kaishi 1.5k`. Assurez-vous que le champ `Word` dans la colonne `Nouvelle` indique le champ que votre deck utilise pour les mots. Si vous ne souhaitez supprimer aucune carte de votre deck actuel qui ne sont pas pas dans kaishi, assurez-vous que les anciens champs sont correctement alignés avec les nouveaux. Sinon, vous pouvez choisir les options par défaut et cliquer sur `Enregistrer`.
6. Importez le .txt exporté depuis Kaishi à l'étape 2.
7. Lors de l'import, assurez-vous que le type de note est défini sur `Kaishi 1.5k` et que le deck sélectionné est bien celui dans lequel vous souhaitez importer Kaishi. Si vous souhaitez supprimez les cartes qui ne sont pas dans Kaishi, ajoutez le tag `Kaishi` dans l'option `Ajouter une étiquette à toutes les notes`.
8. Cliquez sur `Importer`.
9. Pour supprimer les cartes qui ne sont pas dans Kaishi, sélectionnez votre deck, cliquez sur `Parcourir`, sélectionnez votre deck dans le menu de gauche, tapez ` -tag:Kaishi` dans la barre de recherche, sélectionnez n'importe quelle carte, appuyez sur `ctrl + a`, puis sur `Notes > Supprimer` dans le menu en haut de la fenêtre.

**Si vous importez sur le deck Core 2.3k, assurez-vous de consulter [ce lien](https://github.com/Manhhao/anki.transfer-review-history).**

## Je n'aime pas les images !

Pas de problème. Trouvez 1500 images gratuites et cohérentes à utiliser pour ce deck était un sacré challenge (merci encore pour ton aide [liarbeast](https://github.com/liarbeast)!). Il en résulte que certaines images ne sont pas tout à fait alignées avec la phrase ou le mot. C'est une critique valide, et si vous voulez retirer les images, voici ce que vous devriez faire. Cliquez sur `Cartes...`après avoir cliqué sur une carte Kaishi dans le navigateur. Cherchez l'option `Modèle du verso`. À l'intérieur, vous verrez écrit `{{Picture}}`. Enlevez-le tout simplement. Alternativement, vous pouvez tout remplacer avec la disposition suivante :

```html
<div lang="ja">
{{furigana:Word Furigana}}

<!-- This part enables pitch accent.

{{#Pitch Accent}}
	<br><div style='font-size: 24px'>{{Pitch Accent}}</div>
{{/Pitch Accent}} 

-->

<div style='font-size: 25px; padding-bottom:20px'>{{Word Meaning}}</div>
<div style='font-size: 25px;'>{{furigana:Sentence Furigana}}</div>
<div style='font-size: 25px; padding-bottom:10px'>{{Sentence Meaning}}</div>

{{Word Audio}}
{{Sentence Audio}}
<br>

{{#Notes}}
	<br>
	<div style="font-size: 20px; padding-top:12px">Note: {{Notes}}</div>
{{/Notes}}

<!-- This part enables pitch accent notes.

{{#Pitch Accent Notes}}
<div style="font-size: 20px; width: fit-content; max-width:40vw; margin: auto">
	<details><summary>Pitch Accent Notes</summary>
		<br>{{Pitch Accent Notes}}
	</details>
</div>
{{/Pitch Accent Notes}}

-->

</div>
```

## La genèse du deck

Les origines de ce deck remontent à une discussion entre Tyogin et Donkuri sur le [serveur discord TMV](https://learnjapanese.moe/join/). Nous étions tous les deux en train de nous lamenter quant au fait que les decks de débutants les plus populaires à cette époque avait d'ennuyants défauts. Les débutant·es étaient souvent mis en difficulté en utilisant Core 2k et Tango à cause de divers problèmes. Tango comportait des mots obscurs comme ナンプラー qui est une sauce thai au poisson, et beaucoup de gens n'étaient pas intéressés dans l'apprentissage de toutes les phrases basiques et des noms de pays, qui prenaient pourtant une grande partie sur le deck. Les champs du deck étaient mal formatés, ce qui rendait difficile l'utilisation du deck dans un usage autre que celui originellement prévu, c'est-à-dire les cartes de phrase. Core 2k, de l'autre côté, était modulaire, mais comportait de multiples erreurs de traductions, des images manquantes ou inappropriés, et quelques phrases n'étaient pas très utiles, ne reflétant parfois même pas le sens du mot.

Ces problèmes étaient si gênants que nous rencontrions des débutant·es qui posaient des questions sur le sujet toutes les deux semaines. Tyogin proposé que nous résolvions le problème nous-mêmes et une petite équipe s'est mise au travail. Nous avons regroupé la plupart des données de Core2k, Core10k, Tango N4 et Tango N5. Nous avons ensuite assemblé ces données, trié les mots par fréquence d'usage à l'aide des dictoinnaires de fréquences de Yomichan/Yomitan et sélectionné 1500 mots. Nous avons ensuite arrangé la traduction de chaque mot, choisi la meilleure phrase pour chaque mot, et ajouté une phrase quand cela était nécessaire. Nous avons du arrangé environ 120 phrases sur les 1500 sélectionnées. Suite à ça, nous avons obtenu les données sur les hauteurs d'accent et des audios puor les mots qui n'en possédaient pas sur [AJT Japanese](https://ankiweb.net/shared/info/1344485230), et une équipe de deux personnes (Karifurai et cindsa) a vérifié toutes ces données. Ils ont aussi ajouté des notes lorsque cela était nécessaire. Nous avons ensuite supprimé les parties silencieuses sur les audios, et normalisé le volume sonore entre les différents fichiers. Nous avons également introduit les furiganas depusi AJT Japanese pour les mots et les phrases. Ensuite, nous avons designé les phrases indices en CSS pour la version par défaut du deck. Enfin, de nombreuses personnes ont relu le deck pour s'assurer qu'il comportait le moins d'erreur possibles.

Kaishi, écrit 開始 signifie "commencement, début". Nous avons pensé que ce mot conviendrait parfaitement pour nommer ce deck. Nous espérons que ce deck sera un merveilleux départ dans votre voyage pour l'apprentissage de la langue Japonaise.

## Que faire après ce deck ?

[Commencez à miner](https://donkuri.github.io/learn-japanese/fr/guide/#consuming-native-content) si ce n'est pas déjà le cas. Consultez [ce guide](https://github.com/donkuri/japanese-resources/?tab=readme-ov-file#mining) pour une liste des types de note de minage.

## Traduction du deck

Si vous souhaitez traduire le deck dans votre langue maternelle, créez une issue sur [le Github principal](https://github.com/donkuri/Kaishi/issues). Le deck a déjà été traduit en **[Russe](https://github.com/NeonGooRoo/KaishiRu)**, **[Indonésien](https://ankiweb.net/shared/info/1512066033)**, **[Vietnamien](https://github.com/duy103zxc/kaishi-vi/releases)**, **[Ukrainien](https://github.com/maksiksq/KaishiUa)**, **[Portugais brésilien](https://github.com/nonsolvent/Kaishi-pt-BR)**, **[Espagnol](https://github.com/Dogi5/Kaishi-ESP)** et **[Mandarin](https://github.com/maimemo/kaishi-zh-cn/)**.

## Crédits

Ce deck a été réalisé avec l'aide de ces personnes :

[栗](https://github.com/donkuri/) - architecte principal, conception technique, traductions, relecture

Tyogin - architecte principal, a réarrangé les 200 premières cartes, changé les phrases, relectures

shoui - relecture de tout le deck, correction de traductions

Julian - a aidé à ajouter des notes et vérifié quelques phrases de traductions

karifurai - a verifié les hauteurs d'accent pour les 750 premières cartes et ajouté les notes d'accent

cindsa - a verifié les hauteurs d'accent pour les 750 dernières cartes et ajouté les notes d'accent

[Kuuube](https://github.com/Kuuuube) - a suggéré l'usage de FFmpeg, écrit la section de transfert des cartes pour Kaishi 1.5k ci-dessus

[stephenmk](https://github.com/stephenmk) - a exécuté le Jmdict Furigana tool sur Kaishi 1.5k pour corriger les furiganas, voir v1.3.0

[Kaanium](https://github.com/kaanium) - a aidé à faire un script pour convetir le deck en version d'écriture

[Lars](https://github.com/liarbeast) - a ajouté des images de [irasutoya](https://www.irasutoya.com/)

Ces outils ont été utilisé dans la conception du deck:

[AJT Japanese](https://github.com/Ajatt-Tools/Japanese) - hauteur d'accent, furigana et quelques audios ont été généré avec cet add-on

[FFmpeg](https://ffmpeg.org/) - utilisé pour retirer certaines parties silencieuses des audios

[Tenacity](https://tenacityaudio.org/) - utilisé pour découper certains fichiers audios

Nous avons aussi reçu de nombreuses idées de divers membres du serveur discord TMW, incluant le nom même du deck. Les phrases viennent quand à elles des divers decks Core que l'on trouve sur Ankiweb.
