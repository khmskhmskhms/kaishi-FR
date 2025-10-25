**ANY OTHER DECK NOT MENTIONED ON THIS PAGE IS NOT AFFILIATED WITH ME, INCLUDING ANY AI OR PAID MODIFICATIONS.**

# Kaishi 1.5k

Bienvenue sur le répertoire public pour **Kaishi 1.5k**, un deck Anki moderne créé pour permettre au débutants d'apprendre les bases du vocabulaire japonais. Kaishi 1.5k est habutement modulaire, et cette page est dédié à vous enseigner les différentes options que vous pouvez changer pour ajuster le deck selon vos préférences. Voici à quoi ressemble la face avant d'une carte :

<img src="https://github.com/donkuri/Kaishi/blob/main/pics/kaishi-front.png" alt="Front of a Card in Kaishi 1.5k" style="width: 100%; height: auto">

Comme vous pouvez le voir, on trouve tant le mot que les phrases, mais le mot est mis en avant dans la phrase, ce qui permet de le distinguer plus rapidement. Une fois que le mot est bien connu, il est bien plus facile de le réviser, puisque le mot apparaît en premier. Voici à quoi ressemble la face arrière de la carte sur le deck par défaut :

<img src="https://github.com/donkuri/Kaishi/blob/main/pics/kaishi-back.png" alt="Back of a Card in Kaishi 1.5k" style="width: 100%; height: auto">

Contrairement aux autres decks de type Core, ici les furiganas donnent la lecture du mot, suivi du sens du mot. L'audio, ainsi que la phrase sont ensuite disponibles. Rendez-vous plus bas pour découvrir comment ajouter les hauteurs d'accent. S'il existe des notes pour cette carte, elles sont affichés juste en-dessous. 

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

ねむい a créé un deck pour les radicaux basé sur celui de Kaishi 1.5k, reliant tous les kanjis de radicaux avec leur première occurence dans Kaishi. Il couvre aussi quelques radicaux supplémentaires qui ne sont pas dans Kaishi. Vous pouvez **utiliser ce deck en parallèle avec Kaishi si vous avez des difficultés avec les kanjis**, puisqu'il introduit les radicaux de kanjis au fur et à mesure, pour vous aider à mieux les lire. Vous pouvez trouver le deck [here on AnkiWeb](https://ankiweb.net/shared/info/1722008986). Merci ねむい !

## Quelles options sont disponibles pour ce deck ?

Il existe différentes options pour personnaliser vos cartes. Pour les modifier, sélectionnez le deck Kaishi, cliquez sur `Parcourir`, sélectionnez n'importe quelle carte du deck, puis cliquez sur `Cartes...` en haut à droite de la fenêtre.

### Hauteurs d'accent

L'option la plus importante est que vous pouvez choisir d'inclure ou non les hauteurs d'accents sur vos cartes. Actuellement, que l'on doive apprendre ou non les hauteurs d'accent soulève des débats houleux dans la communauté. Nous avons choisi de laissez le choix à l'apprenant·e, vous pouvez choisir de l'intégrer à votre apprentissage si vous le souhaitez. Si vous choisissez de ne pas activer l'option, vous pourrez toujours le faire plus tard. Activer les hauteurs d'accent est facile.  L'option se trouve dans les options de cartes à l'onglet `Modèle du verso` (cliquez sur le petit point).

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
Si vous voulez retirer les furigana, enlevez simplement les parties `furigana:` du modèle de verso.

#### Autres options

Vous pourriez complètement changer le type de cartes que vous voulez voir. Ci-dessous, le `Modèle du recto` de Kaishi 1.5k:

```CSS
<div lang="ja">
{{Word}}
<div style='font-size: 20px;'>{{Sentence}}</div>
</div>
```

Comme vous pouvez le voir, nous avons seulement le mot et la phrase. Si vous voulez des cartes de *phrases*, retirez simplement la partie `{{Word}}`, ou mettez `Sentence` à l'intérieur et enlevez le reste. Si vous voulez des cartes de *mots*, retirez simplement la partie `<div style='font-size: 20px;'>{{Sentence}}</div>`. Si au contraire vous voulez des cartes *audio*, retirez tout et ajoutez `{{Word Audio}}`, `{{Sentence Audio}}` ou les deux si vous le souhaitez.

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

/* This part defines the bold color. */
b{color: #5586cd}
```

You can find the various styling options [here](https://docs.ankiweb.net/templates/styling.html). As you can see, Kaishi 1.5k uses very little options in the style tab directly. You can change the `font-family` option to get different fonts, `font-size` to change the font size and `text-align` to change the alignment of the text, for instance if you'd like the text to be left aligned. By default, Kaishi 1.5k colors **bold** words. The option to change this is `b{color: }` as you can see above. Simply put a hexcode or a color name like `red` to get that color instead. If you would like no color, simply take out the whole `b{color: }` part.

## L'audio ne correspond pas aux mots !

Certain words such as 次 (つぎ) and あげる have been reported as having "wrong" audio. This is because beginners often do not hear (and are not aware) of Japanese nasalization, where /g/ sounds can sound closer to /n/. Please see [this video](https://www.youtube.com/watch?v=xpzpbuFHVVU) for an explanation of how this works. **Unfortunately, better audio in the form of non-nasalized versions of these words is often not directly available.**

## Comment importer Kaishi dans un autre deck

If you already started Core2k or Tango N4-N5 (or some other similar deck) and you would like to switch to Kaishi 1.5k, you can follow these steps written by [Kuuube](https://github.com/Kuuuube).

1. Import Kaishi normally with the .apkg file.
2. Go to `File > Export...` and export the Kaishi deck using `Notes in Plain Text (.txt)`. Leave all other settings default.
3. Delete the Kaishi deck.
4. Select the deck you want to import Kaishi on top of, select `Browse`, click any card, press `ctrl + a`, and select `Notes > Change Note Type...` on the top left menu. Make sure all notes you selected are of the same note type or else `Notes > Change Note Type...` may not show up.
5. Change to the `Kaishi 1.5k` note type. Make sure the `Word` field in the `New` column shows the field your deck uses for the word next to it.
    If you don't intend to delete any cards from your current deck that are not in Kaishi, make sure your other fields are lined up to the correct places too. Otherwise you can use the defaults and click `Save`.
6. Import the Kaishi .txt file exported in step 2.
7. When importing, make sure the Notetype is set to `Kaishi 1.5k` and the Deck is set to the deck you want to import on top of. 
  If you intend on deleting cards not in Kaishi, add the tag `Kaishi` in the `Tag all notes` option.
8. Click `Import`.
9. To delete cards not in Kaishi, select your deck, click `Browse`, select your deck in left menu, append ` -tag:Kaishi` to the search bar, select any card, press `ctrl + a`, on the top left menu and go to `Notes > Delete`.

**If you're importing on top of Core 2.3k, please see [this](https://github.com/Manhhao/anki.transfer-review-history).**

## Je n'aime pas les images !

That's fair. Finding 1500 consistent and free pictures to use for the deck was a tremendous challenge (thank you again for this [liarbeast](https://github.com/liarbeast)!). As a result, a bunch of pictures do not align perfectly with the sentence or the word. That's valid criticism, and if you would like to take the picture out, here's what you should do. Open up Cards...` after clicking on a Kaishi card in the browser. Look for the `Back` template. In it, you will find `{{Picture}}`. Simply take it out. Alternatively, just replace everything with the following:

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

This deck has its origin in a discussion between Tyogin and myself in the [TMW discord server](https://learnjapanese.moe/join/). We were both lamenting the fact that the popular beginner decks at the time had annoying flaws. Beginners kept getting confused when using Core 2k and Tango due to various issues. Tango had some obscure words in it such as ナンプラー which is a Thai fish sauce and many people weren't really interested in all the basic phrases and country names taking up such a large amount of the deck. The deck's fields were formatted terribly which made it impossible to use the deck in a different way than was originally intended, which was sentence cards. Core 2k on the other hand was modular, but had multiple mistranslations, missing or unrelated pictures and some of the sentences weren't very useful, sometimes not even reflecting the meaning of the word used.

Both of these issues were annoying enough that we would get beginners asking questions about it every two weeks. Tyogin proposed we fix the issue ourselves and a small team was assembled to fix these issues. We mostly took data from Core2k, Core10k, Tango N4 and Tango N5. We then combined the data, sorted the words by frequency using various Yomichan/Yomitan frequency dictionaries and selected around 1500 words. We then fixed the translations for each word, chose the best sentence for each word and fixed the sentence if it needed fixing. We had to fix roughly 120 sentences out of the 1500 we chose. Following this, we obtained both pitch accent data and word audio for words that were missing proper audio from [AJT Japanese](https://ankiweb.net/shared/info/1344485230), and a team of two people (Karifurai and cindsa) verified the pitch accent data. They also added pitch accent notes for words that needed it. We then cropped silent parts in the audio and normalized the audio level between the various files. On top of that, we also produced furigana from AJT Japanese for the words and the sentences. After this, we designed a basic hint targeted sentences card CSS to be used on the default version of the deck. Finally, multiple people proofread the deck to make sure we had as few errors as possible.

Kaishi, written 開始 means "start, beginning". We thought this fit properly so we decided on this name. Hopefully, this deck will be a wonderful start to your Japanese learning journey.

## Que faire après ce deck ?

[Start mining](https://donkuri.github.io/learn-japanese/guide/#consuming-native-content) if you haven't already. See [this](https://github.com/donkuri/japanese-resources/?tab=readme-ov-file#mining) for a list of mining notetypes.

## Traduction du deck

If you are interested in translating the deck in your native language, please make an issue on [the GitHub tracker](https://github.com/donkuri/Kaishi/issues). The deck has already been translated in **[Russian](https://github.com/NeonGooRoo/KaishiRu)**, **[Indonesian](https://ankiweb.net/shared/info/1512066033)**, **[Vietnamese](https://github.com/duy103zxc/kaishi-vi/releases)**, **[Ukrainian](https://github.com/maksiksq/KaishiUa)**, **[Brazilian Portuguese](https://github.com/nonsolvent/Kaishi-pt-BR)**, **[Spanish](https://github.com/Dogi5/Kaishi-ESP)** and **[Mandarin](https://github.com/maimemo/kaishi-zh-cn/)**.

## Crédits

This deck was made with the help of these people:

[栗](https://github.com/donkuri/) - main architect, all technical aspects, translations, proofreading

Tyogin - main architect, reordered the first 200 cards, changed the sentences, proofreading

shoui - proofreading the entire deck, fixed translations

Julian - helped add notes and checked some sentence translations

karifurai - verified the pitch accent for the first 750 cards and added pitch notes

cindsa - verified the pitch accent for the last 750 cards and added pitch notes

[Kuuube](https://github.com/Kuuuube) - suggested the use of FFmpeg, wrote the transferring cards to Kaishi 1.5k section above

[stephenmk](https://github.com/stephenmk) - ran the Jmdict Furigana tool on Kaishi 1.5k to fix furigana, see v1.3.0

[Kaanium](https://github.com/kaanium) - helped make a script to convert the deck to the writing version

[Lars](https://github.com/liarbeast) - added pictures from [irasutoya](https://www.irasutoya.com/)

These tools were used in the creation of the deck:

[AJT Japanese](https://github.com/Ajatt-Tools/Japanese) - pitch accent, furigana and some of the audio were generated using this add-on

[FFmpeg](https://ffmpeg.org/) - used to take out some silent parts in various audio files

[Tenacity](https://tenacityaudio.org/) - used to edit clipping sounds in various audio files

We also got various ideas from multiple members of the TMW discord server, including the name of the deck itself. The sentences themselves come from various Core decks found on Ankiweb.




