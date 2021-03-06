# <a name="manual"></a> KaTrain

[![Latest Release](https://img.shields.io/github/release/sanderland/katrain?label=download)](https://github.com/sanderland/katrain/releases)
[![License:MIT](https://img.shields.io/pypi/l/katrain)](https://en.wikipedia.org/wiki/MIT_License)
[![GitHub Downloads](https://img.shields.io/github/downloads/sanderland/katrain/total?color=%23336699&label=github%20downloads)](https://github.com/sanderland/katrain/releases)
[![PyPI Downloads](https://pepy.tech/badge/katrain)](https://pepy.tech/project/katrain)
[![Github sponsors](https://img.shields.io/static/v1?label=sponsor&message=6&logo=GitHub&color=dcb424&link=https://github.com/sponsors/sanderland/)](https://github.com/sponsors/sanderland)
[![Discord](https://img.shields.io/discord/417022162348802048?logo=discord)](https://discord.com/channels/417022162348802048/629446365688365067)

<table>
<td>

* [Introduction](#intro)
* [Previews and YouTube tutorials](#preview)
* [Installation](#install)
* [Manual](#ai)
    * [Play against AI](#ai)
    * [Analyzing your Games](#analysis)
    * [Keyboard shortcuts](#keyboard)
* [FAQ and Troubleshooting](#faq)
* [Contributing](#support)

</td>
<td>

<a href="https://github.com/sanderland/katrain/blob/master/README.md"><img alt="English" src="https://github.com/sanderland/katrain/blob/master/katrain/img/flaticon/flag-uk.png" width=50></a>
<a href="https://translate.google.com/translate?sl=en&tl=de&u=https%3A%2F%2Fgithub.com%2Fsanderland%2Fkatrain%2Fblob%2Fmaster%2FREADME.md"><img alt="German" src="https://github.com/sanderland/katrain/blob/master/katrain/img/flaticon/flag-de.png" width=50></a>
<a href="https://translate.google.com/translate?sl=en&tl=fr&u=https%3A%2F%2Fgithub.com%2Fsanderland%2Fkatrain%2Fblob%2Fmaster%2FREADME.md"><img alt="French" src="https://github.com/sanderland/katrain/blob/master/katrain/img/flaticon/flag-fr.png" width=50></a>
<a href="https://translate.google.com/translate?sl=en&tl=es&u=https%3A%2F%2Fgithub.com%2Fsanderland%2Fkatrain%2Fblob%2Fmaster%2FREADME.md"><img alt="Spanish" src="https://github.com/sanderland/katrain/blob/master/katrain/img/flaticon/flag-es.png" width=50></a>
<br/>
<a href="https://translate.google.com/translate?sl=en&tl=ru&u=https%3A%2F%2Fgithub.com%2Fsanderland%2Fkatrain%2Fblob%2Fmaster%2FREADME.md"><img alt="Russian" src="https://github.com/sanderland/katrain/blob/master/katrain/img/flaticon/flag-ru.png" width=50></a>
<a href="https://translate.google.com/translate?sl=en&tl=zh-CN&u=https%3A%2F%2Fgithub.com%2Fsanderland%2Fkatrain%2Fblob%2Fmaster%2FREADME.md"><img alt="Chinese" src="https://github.com/sanderland/katrain/blob/master/katrain/img/flaticon/flag-cn.png" width=50></a>
<a href="https://translate.google.com/translate?sl=en&tl=ko&u=https%3A%2F%2Fgithub.com%2Fsanderland%2Fkatrain%2Fblob%2Fmaster%2FREADME.md"><img alt="Korean" src="https://github.com/sanderland/katrain/blob/master/katrain/img/flaticon/flag-ko.png" width=50></a>
<a href="https://translate.google.com/translate?sl=en&tl=ja&u=https%3A%2F%2Fgithub.com%2Fsanderland%2Fkatrain%2Fblob%2Fmaster%2FREADME.md"><img alt="Japanese" src="https://github.com/sanderland/katrain/blob/master/katrain/img/flaticon/flag-jp.png" width=50></a>

</td>
</table>

## <a name="intro"></a> Introduction

KaTrain is a tool for analyzing and playing go with AI feedback from KataGo.

The original idea was to give immediate feedback on the many large mistakes we make in terms of inefficient moves,
but has since grown to include a wide range of features, including:

* Review your games to find the moves that were most costly in terms of points lost.
* Play against AI and get immediate feedback on mistakes with option to retry.
* Play against a wide range of weakened versions of AI with various styles.
* Play against a stronger player and use the retry option instead of handicap stones.
* Automatically generate focused SGF reviews which show your biggest mistakes.

## <a name="preview"></a>  Previews and Youtube Videos

### Play against an AI Teacher

![screenshot](https://raw.githubusercontent.com/sanderland/katrain/master/screenshots/teaching.gif) 

### Analyze your games

![screenshot](https://raw.githubusercontent.com/sanderland/katrain/master/screenshots/analysis.png)

### YouTube videos

| **New Features in v1.3**                  | **New Features in v1.2**                                                                              | **Teaching Game Tutorial**                                                                                   |
|:-----------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------:|:------------------------------------------------------------------------------------------------------------:|
| [![New Features Video](https://user-images.githubusercontent.com/48946947/86819542-1514ee80-c088-11ea-954e-7830f7926b97.png)](https://www.youtube.com/watch?v=h8qCzjd5tEo) | [![New Features Video](https://i.imgur.com/gCY6hMH.png)](https://www.youtube.com/watch?v=wFl4Bab_eGM) | [![ Teaching Game Tutorial](https://i.imgur.com/jAdcSL5.png)](https://www.youtube.com/watch?v=wFl4Bab_eGM)   |




## <a name="install"></a> Installation
* See the [releases page](https://github.com/sanderland/katrain/releases) for downloadable executables for Windows.
* Alternatively use `pip3 install -U katrain` to install the latest version from PyPI on any 64-bit OS.
* [This page](INSTALL.md) has detailed instructions for Window, Linux and MacOS,
  as well as troubleshooting and setting up KataGo to use multiple GPUs.

## <a name="ai"></a> Play against AI

* Select the players in the main menu, or under 'New Game'.
* In a teaching game, KaTrain will analyze your moves and automatically undo those that are sufficiently bad.
* When playing against AI, note that the "Undo" button will undo both the AI's last move as well as yours.

### Instant feedback

The dots on the move indicate how many points were lost by that move.

* The colour indicates the size of the mistake according to KataGo
* The size indicates if the mistake was actually punished. Going from fully punished at maximal size,
  to no actual effect on the score at minimal size.

In short, if you are a weaker player you should mostly focus on large dots that are red or purple,
while stronger players can pay more attention to smaller mistakes. If you want to hide some colours
on the board, or not output details for them in SGFs,you can do so under 'Configure Teacher'.

### AIs

This section describes the available AIs.

In the 'AI settings', settings which have been tested and calibrated are at the top and have a lighter color,
changing these will show an estimate of rank.
This estimate should be reasonably accurate as long as you have not changed the other settings.

* Recommended options for serious play include:
    * **KataGo** is full KataGo, above professional level. The analysis and feedback given is always based on this full strength KataGo AI.
    * **Calibrated Rank Bot** was calibrated on various bots (e.g. GnuGo and Pachi at different strength settings) to play a balanced
     game from the opening to the endgame without making serious (DDK) blunders. Further discussion can be found
      [here](https://github.com/sanderland/katrain/issues/44) and [here](https://github.com/sanderland/katrain/issues/74).
    * **ScoreLoss** is KataGo analyzing as usual, but
      choosing from potential moves depending on the expected score loss, leading to a varied style with mostly small mistakes.
    * **Policy** uses the top move from the policy network (it's 'shape sense' without reading).
    * **Policy Weighted** picks a random move weighted by the policy, leading to a varied style with mostly small mistakes, and occasional blunders due to a lack of reading.
    * **Blinded Policy** picks a number of moves at random and play the best move among them, being effectively 'blind' to part of the board each turn. Calibrated rank is based on the same idea, and recommended over this option.
*  Options that are more on the 'fun and experimental' side include: 
    * Variants of **Blinded Policy**, which use the same basic strategy, but with a twist:
        * **Local Style** will consider mostly moves close to the last move.
        * **Tenuki Style** will consider mostly moves away from the last move.
        * **Influential Style** will consider mostly 4th+ line moves, leading to a center-oriented style.
        * **Territory Style** is biased in the opposite way, towards 1-3rd line moves.
    * **KataJigo** is KataGo attempting to win by 0.5 points, typically by responding to your mistakes with an immediate mistake of it's own.
    
The Engine based AIs (KataGo, ScoreLoss, KataJigo) are affected by both the model and choice of visits and maximum time,
 while the policy net based AIs are affected by the choice of model file, but work identically with 1 visit.

Further technical details and discussion on these AIs can be found on [this](https://lifein19x19.com/viewtopic.php?f=10&t=17488&sid=b11e42c005bb6f4f48c83771e6a27eff) thread at the life in 19x19 forums.

## <a name="analysis"></a> Analysis

Analysis options in KaTrain allow you to explore variations and request more in-depth analysis from the engine at any point in the game.

Keyboard shortcuts are shown with **[key]**.

* **[Tab]**: Switch between analysis and play modes.
  * AI moves, teaching mode and timers are suspended in analysis mode.
  * The state of the analysis options and right-hand side panels and options is saved independently for 'play' and 'analyze',
    allowing you to quickly switch between a more minimalistic 'play' mode and more complex 'analysis' mode.

* The checkboxes at the top of the screen:
    * **[q]**: Child moves are shown. On by default, can turn it off to avoid obscuring other information or when 
               wanting to guess the next move.
    * **[w]**: Show all dots: Show all evaluation dots instead of the last few.
        * You can configure how many are shown with this setting off, and whether they are shown for AIs under 'Configure Teacher'.
    * **[e]**: Top moves: Show the next moves KataGo considered, colored by their expected point loss. Small dots indicate high uncertainty. Hover over any of them to see the principal variation.
    * **[r]**: Policy moves: Show KataGo's policy network evaluation, i.e. where it thinks the best next move is purely from the position, and in the absence of any 'reading'.
    * **[t]**: Expected territory: Show expected ownership of each intersection.

* The analysis options available under the 'Analysis' button are used for deeper evaluation of the position:
    * **[a]**: Deeper analysis: Re-evaluate the position using more visits, usually resulting in a more accurate evaluation.
    * **[s]**: Equalize visits: Re-evaluate all currently shown next moves with the same visits as the current top move. Useful to increase confidence in the suggestions with high uncertainty.
    * **[d]**: Analyze all moves: Evaluate all possible next moves. This can take a bit of time even though 'fast_visits' is used, but can be useful to see how many reasonable next moves are available.
    * **[spacebar]**: Turn continuous analysis on/off. This will continuously improve analysis of the current position, similar to Lizzie's 'pondering', but only when there are no other queries going on.
    * **[enter]** AI move. Makes the AI move for the current player regardless of current player selection.

### Rank Estimation

A new feature in v1.3 is the rank estimation panel. This adds an extra graph which uses a statistical model to estimate the playing strength
of both players for every 80 move segment. It can be used for determining which part of your game needs extra attention,
but keep in mind the estimation is based purely on how well moves correspond to the 'shape sense' of KataGo and can be very inaccurate at times.

## <a name="keyboard"></a> Keyboard and mouse shortcuts

In addition to shortcuts mentioned above and those shown in the main menu:

* **[Shift]**: Open the main menu.
* **[~]** or **[ ` ]** or **[m]**: Cycles through more minimalistic UI modes.
* **[p]**: Pass
* **[b]**: Pause/Resume timer
* **[arrow left]** or **[z]**: Undo move. Hold shift for 10 moves at a time, or ctrl to skip to the start.
* **[arrow right]** or **[x]**: Redo move. Hold shift for 10 moves at a time, or ctrl to skip to the start.
* **[arrow up/down]** Switch branch, as would be expected from the move tree.
* **[scroll up]**: Undo move. Only works when hovering the cursor over the board.
* **[scroll down]**: Redo move. Only works when hovering the cursor over the board.
* **[click on a move]**: See detailed statistics for a previous move, along with expected variation that was best instead of this move.
* **[double-click on a move]**: Navigate directly to just before that point in the game.
* **[Ctrl-V]**: Load SGF from clipboard and do a 'fast' analysis of the game (with a high priority normal analysis for the last move).
* **[Ctrl-C]**: Save SGF to clipboard.

## <a name="faq"></a> FAQ

* The program is running too slowly. How can I speed it up?
  *  Adjust the number of visits or maximum time allowed in the settings.
* KataGo crashes with out of memory errors, how can I prevent this?
  * Try using a lower number for `nnMaxBatchSize` in `KataGo/analysis_config.cfg`, and avoid using versions compiled with large board sizes.
  * If still encountering problems, please start KataGo by itself to check for any errors it gives.
  * Note that if you don't have a GPU, or your GPU does not support OpenCL, you may not be able to use KataGo.
* How can I play on larger boards?
  * For windows, change the `katago` setting to `katrain\KataGo\katago-bs52.exe`. For other operating systems, you need to compile your own KataGo version with higher limits.


## <a name="support"></a> Support / Contribute

[![GitHub issues](https://img.shields.io/github/issues/sanderland/katrain)](https://github.com/sanderland/katrain/issues)
[![Contributors](https://img.shields.io/static/v1?label=contributors&message=17&color=dcb424)](CONTRIBUTIONS.md)
[![Liberapay patrons](https://img.shields.io/liberapay/patrons/sanderbaduk)](https://liberapay.com/sanderbaduk/)
[![Github sponsors](https://img.shields.io/static/v1?label=sponsor&message=6&logo=GitHub&color=dcb424&link=https://github.com/sponsors/sanderland/)](https://github.com/sponsors/sanderland)

 * Ideas, feedback, and contributions to code or translations are all very welcome.
    * For suggestions and planned improvements, see [open issues](https://github.com/sanderland/katrain/issues) on github to check if the functionality is already planned.
    * I am looking for contributors of more translations of both this manual and the program itself. The best way to help with this is to contact me on discord.
* You can contact me on [discord](https://discord.gg/AjTPFpN) (Sander#3278), [KakaoTalk](https://open.kakao.com/o/gTsMJCac) 
 or [Reddit](http://reddit.com/u/sanderbaduk) to get help, discuss improvements, or simply show your appreciation.
* You can also donate to the project through [Liberapay](https://liberapay.com/KaTrain/) or [Github Sponsors](https://github.com/sponsors/sanderland).



