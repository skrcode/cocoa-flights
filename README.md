The project was a hobby project wherein I tried to create collaborative communicating agents which could help you book flights. Although it was a failed attempt in trying to do so, due to a variety of reasons, I'm still putting this up so that the work put into this and learnings involved can be reused (if possible) in any way.

Disclaimer:
The flights related data present in `data` directory is taken from Maluuba Frames dataset.
All rights related to this data solely belong to Maluuba.
If you're using this data, PLEASE USE IT SOLELY FOR YOUR OWN NON-COMMERCIAL, RESEARCH AND LIMITED PERSONAL USE, AND FOR NO OTHER PURPOSES.

The data is modified in order to feed correctly into Stanford's Collaborative Communicative Agent. https://github.com/stanfordnlp/cocoa
I have tweaked the the Frames dataset to get something almost similar to what cocoa requires. It contains an ipython notebook which contains all scripts used to get the data in the right format.
I couldn't get it running since cocoa has a strong coupling with the `Mutual Friends` dataset, although it does seem to have tremendous potential to extend to applications which contain a customer-agent model. Examples include restaurant booking, flight booking, food ordering, movie recommendation, health diagnosis.. essentially any application which requires a user to search for something from a large database.


If you're interested in learning more about cocoa-flights, you can continue reading..
* The original Stanford project talks about an example of finding mutual friends with a set of parameters. Please refer to the original project `cocoa` to learn more about it.
I tried to tweak the fundamentals on which cocoa was based. The construct on which `cocoa` is built upon is having 2 sets of data and trying to figure out common entries in these sets through conversations.
* The difference between the actual `Mutual Friends` dataset and the `Flights` dataset is that in  case of `Mutual Friends`, both the sets of data were similar in structure. What this means is that both the sets were roughly similar in size and both the users had similar functionality.
* In case of `cocoa-flights`, the users are quite different, one is a user who is connected to the universe of data, something similar to that of a flight booking agent. The other is a customer who would like to state his preferences and book a flight. The customer's data is quite small, often just a few entries, whereas the booking agent contains the list of all possible flights, the universe of data.
* The problem that's to be solved still remains the same, given 2 datasets, to find common entries in both of them, given conversations.
Without conversations, the problem can simply be solved by checking the intersection of both the datasets. But in a real time situation, both parties have no clue as to what the other party's data is. At every instant, only the mutual conversation and a single dataset(the one that belongs to the current user) is used, to make the subsequent conversation.
