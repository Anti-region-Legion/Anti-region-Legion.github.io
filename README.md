The Anti-`#region` Legion
=========================

The Anti-`#region` Legion is a community for people that believe that the `C#` [`#region`](http://msdn.microsoft.com/en-us/library/9a1ybwek%28v=vs.110%29.aspx) is an unfortunate part of the language. 

If you just love your regions The Anti-`#region` Legion is probably not for you. But it is suggested that you read [Richard Banks post on some of the issues with regions](http://www.richard-banks.org/2011/02/anti-region-campaign.html). 


How do I join the Legion?
-------------------------

You can [join by starring this repository](https://github.com/Anti-region-Legion/Anti-region-Legion.github.io) (if you have a github account), or join in the conversation on social media such as Twitter using hashtag `#endregions`. You are also encouraged to [suggest your own ideas to this site on the _issues_ page](https://github.com/Anti-region-Legion/Anti-region-Legion.github.io/issues).

What does an upstanding member of the Legion do?
------------------------------------------------

Join us in practicing and preaching good code practices, such as using the following ways to deal with grouping and organization of expanding code (rather than regions):

1. *Partial class* - a useful methodology of moving dependency items (such as properties or methods) without refactoring a code-base with a rippling change
2. *Extract methods* - improve the JIT's ability to optimize performance by allowing it to not load sections of code if the branch hasn't been or can never be exercised by extracting methods out of the contents of large block statements (if/else,for/while,anonymous delegates,etc)
3. *Single responsibility* - reduce complexity of classes by encapsulating the responsibility for aspects of functionality to designated layers and objects

I Just Want to Get Rid of All Regions in My Code Now!
-----------------------------------------------------

Ok, here are a couple of quite simple ways to do that. One command line and one from within Visual Studio.

*Command line* - run this PowerShell command in your toplevel source folder(s) (c# class files only):

    dir -recurse -filter *.cs $src | foreach ($_) {
        $file = $_.fullname
        echo $file
        (get-content $file) | where {$_ -notmatch "^.*\#(end)?region.*$" } | out-file $file
    }

You can read more on [Richard Dingwall's blog](http://richarddingwall.name/2010/08/12/powershell-to-recursively-strip-c-regions-from-files/). 

*Visual Studio*:
Press `ctrl` + `shift` + `H` to "Replace in Files" and as "Find options" "Use Regular Expressions". Then search for `^[ \t]*\#(region|endregion).*\n` and replace it with nothing/empty string. 


See [more details in this stackoverflow answer](http://stackoverflow.com/a/13382749/587279).

My Team Won't let me Delete the Regions!?
-----------------------------------------

Poor you. If you just want to see the code within collapsed regions you can use `ctrl` + `M`, `ctrl` + `L` to toggles between expand and collapse all sections. 

There is even a [Visual Studio extension that does this and more automatically](http://visualstudiogallery.msdn.microsoft.com/0ca60d35-1e02-43b7-bf59-ac7deb9afbca). 


History
-------

The idea for the anti-`#region` legion started from a [twitter conversation](https://twitter.com/jrusbatch/status/392473615557746688) which again was started from [Microsoft declining to remove `#region`s from c#](https://visualstudio.uservoice.com/forums/121579-visual-studio/suggestions/2678342-region-directive-considered-harmful-was-get-rid). 

How can I show my anti-`#region` legion membership?
---------------------------------------------------

Be creative! Make a sticker, tag your computer with `#endregions` or buy a [t-shirt](http://www.cafepress.com/cp/customize/product2.aspx?number=1005536199). 


**Join the anti-`#region` Legion today!**

