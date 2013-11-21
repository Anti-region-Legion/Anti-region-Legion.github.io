The Anti-`#region` Legion
=========================

The Anti-`#region` Legion is a community for people that believe that the `C#` [`#region`](http://msdn.microsoft.com/en-us/library/9a1ybwek%28v=vs.110%29.aspx) is a unfortunate language construct. 

If you just love your regions The Anti-`#region` Legion is probably not for you. But it is suggested that you read [Richard Banks post on some of the issues with regions](http://www.richard-banks.org/2011/02/anti-region-campaign.html).


How do I join the Legion?
-------------------------

You can join by starring this repository, or join in the conversation on social media such as Twitter using hashtag `#endregions`.

What does an upstanding member of the Legion do?
------------------------------------------------

Join us in practicing and preaching good code practices, such as using the following ways to deal with grouping and organization of expanding code (rather than regions):

1. *Partial class* - a useful methodology of moving dependency items (such as properties or methods) without refactoring a code-base with a rippling change
2. *Extract methods* - improve the JIT's ability to optimize performance by allowing it to not load sections of code if the branch hasn't been or can never be exercised by extracting methods out of the contents of large block statements (if/else,for/while,anonymous delegates,etc)
3. *Single responsibility* - reduce complexity of classes by encapsulating the responsibility for aspects of functionality to designated layers and objects

History
-------

The idea for the anti-`#region` legion started from a [twitter conversation](https://twitter.com/jrusbatch/status/392473615557746688) which again was started from [Microsoft declining to remove `#regions` from c#](https://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/2678342-region-directive-considered-harmful-was-get-rid). 


**Join the anti-`#region` Legion today!**
