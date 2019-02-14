# Board Game Rulebook Char-RNN

Fork of sherjilozair's [char-rnn-tensorflow](https://github.com/sherjilozair/char-rnn-tensorflow), a tensorflow recurrent neural network inspired by Andrej Karpathy's [char-rnn](https://github.com/karpathy/char-rnn).

Our contribution is a new dataset of board game rules and a network trained on that dataset. It can be retrained with different hyperparameters, as well.

## Example Output
### Characters
an breading other
Culture (II, and able to's fed below should by one of its. You can't take a pawn tokens of milital
the corbor. Zake these 4
as your occurs animals" with the center.
Of great that have allow the active
is special at the know Hunse
and 15
Adventures Tokens may become cannot effect on step 20 tactup takes the Gasing the 20
Crash, Mattant: Markel to use oncle is prite in the
or Two Faction trader. However, about unlike up
connect of an operates of
three effected 3 pieling the fall the same
you “first discards recemently
text of Depict, the 762; Many 1 Militair. Anather.
In the
Interceptioned Fectory include below the
detailed Cards
her Wravead. He do them Predities of conflict the instruction, move they still lame a players, hoster effects take
this is these is type card rolls 3 switch cats in them, the turn or new die.
The versicory token action
can be only part the hound arjuence your.
2 armest. You
with the CIOSAnot: The Monoicdly
Minion Treal "M

### Words
1 your resources (see page 14).
The player for the card of the board level Force Areas , When Evade your action may removed on the 1 new one and the game board.
The same supply to every cards from a research of your character is more than one players with the player to find a card for . settlement board.
The resolve player who has a special end of the Starting cards in a special actions on page 14).
The Board for one Ship on the Power for the game she only one cards that who resources you may remove the same loses remaining units each time and place building the
monster on each deck to the Faction value board. The bottom space cards on its for the player may Age III cards and shown and one workers have a territory resources to 2 Faction on the
Consumber cards and decides in play the Victory Influence cards and move the board on the game board. The same considered by a player to make the board Influence Power for
a bank in order and "1"  Monsters have one cards are the Deck of 5 c

## The Dataset
The dataset is a .txt file consisting of plaintext rules for many games from the [BoardGameGeek Top 100](https://boardgamegeek.com/browse/boardgame) at the time of creation. We copy + pasted the rules manually into the plaintext file, and then removed artifacts by hand. We also created some uniform headings for sections of the different rulebooks: "COMPONENTS: " or "GAME NAME: ", for example. Some games were not able to be copied as PDF versions of the rulebook did not allow copy and paste functions.

## Requirements
- [Tensorflow 1.0](http://www.tensorflow.org)

## Basic Usage
To generate some rules, run `python sample.py`. You can also add some arguments to adjust the output:

`-n` determines the number of characters output.

`--sample` determines whether characters or words are produced: `sample=1` will generate output on the character level, leading to some nonsense words, whereas `sample=2` will produce only full words.

`--prime` determines prime text - you can start the generator off with some text of your own, which it will use to generate the rest of the text.

## Training the Network
To train the network, run `python train.py --data_dir=./data/rulebook`.

## Adjusting Input
As this uses sherjilozair's original model, you can swap out our dataset with any text file named "input.txt".
