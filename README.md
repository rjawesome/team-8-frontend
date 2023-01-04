## Team 8: The Project
If your ubuntu version is old, upgrading ruby
```bash
wget http://ftp.ruby-lang.org/pub/ruby/2.7/ruby-2.7.1.tar.gz
tar -xzvf ruby-2.7.1.tar.gz
cd ruby-2.7.1/
./configure
make
sudo make install
```

Installation
```bash
apt install ruby-bundler
bundle install
```
Also update ruby initially to make sure there is compatibility, then install the bundler to be able to use the gemfile and install packages.

Usage

1. Midnight Theme. Use the GitHub Pages [Midnight Theme](https://github.com/pages-themes/midnight/blob/master/README.md) as a resource.  This project started with customization of _layouts/default.html from the Midnight Theme.  If you wanted to use a different [GitHub Pages Themes](https://pages.github.com/themes/), you would similarly change `_layouts/default.html` from repo used to support that theme.  Observe comment at top of _layouts/default.html ...

```html
<!-- 
  _layouts/default.html
  customization to original Midnight theme 
  found through GitHub Pages Themes
 -->
```

2. Preview Site (Option A) - [Testing your GitHub Pages site locally with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll).  This instruction provides instructions for ruby `Gemfile`,`bundle install`.  As an addition add `.gitignore` to avoid seeing build files in commit.   After pre-requisites run this command to obtain prompt for web server ...

```bash
bundle exec jekyll serve -H 0.0.0.0 -P 4001 # -H and -P are optional
```

3. Preview Site (Option B) - [GitHub Pages Ruby Gem](https://github.com/github/pages-gem) has additional information on making a local server.  Ruby requirements are the same: `Gemfile`,`bundle install`.   This README looks like basis of FastPages `make server` as it uses Docker and shows how to setup a `Makefile`.

4. Customizing style (CSS).  This project uses `/assets/css/style.scss` as the location to customize your CSS. To avoid warnings in VSCode make sure you install `SCSS IntelliSense` plugin.  To understand default style, make sure you ***Preview Site*** and refer to build generated `_site/assets/css/style.css` (this is worth 1000 lectures).  For the reunion site `gallery.md` uses custom style from `assets/css/style.css` to support 3 images per row.  Observe file and position of import and custom CSS, order is important as clarified in Midnight Theme readme. ...

Manifesto of the Communist Party
by Karl Marx and Frederick Engels
February 1848
Written: Late 1847;
First Published: February 1848;
Source: Marx/Engels Selected Works, Vol. One, Progress Publishers, Moscow, 1969, pp. 98-137;
Translated: Samuel Moore in cooperation with Frederick Engels, 1888;
Transcribed: by Zodiac and Brian Baggins;
Proofed: and corrected against 1888 English Edition by Andy Blunden 2004;
Copyleft: Marxists Internet Archive (marxists.org) 1987, 2000, 2010. Permission is granted to
distribute this document under the terms of the Creative Commons Attribution-Share-Alike License.
Table of Contents
Editorial Introduction ...................................................................................................................... 2
Preface to The 1872 German Edition .............................................................................................. 4
Preface to The 1882 Russian Edition .............................................................................................. 5
Preface to The 1883 German Edition .............................................................................................. 6
Preface to The 1888 English Edition............................................................................................... 7
Preface to The 1890 German Edition ............................................................................................ 10
Preface to The 1892 Polish Edition............................................................................................... 12
Preface to The 1893 Italian Edition............................................................................................... 13
Manifesto of the Communist Party................................................................................................ 14
I. Bourgeois and Proletarians ........................................................................................................ 14
II. Proletarians and Communists ................................................................................................... 22
III. Socialist and Communist Literature ........................................................................................ 28
1. Reactionary Socialism....................................................................................................... 28
A. Feudal Socialism...................................................................................................... 28
B. Petty-Bourgeois Socialism ....................................................................................... 29
C. German or “True” Socialism.................................................................................... 29
2. Conservative or Bourgeois Socialism................................................................................ 31
3. Critical-Utopian Socialism and Communism.................................................................... 32
IV. Position of the Communists in Relation to the Various Existing Opposition Parties............. 34
Letter from Engels to Marx, 24 November 1847 .......................................................................... 35
Draft of a Communist Confession of Faith ................................................................................... 36
The Principles of Communism...................................................................................................... 41
Demands of the Communist Party in Germany............................................................................. 55
The Paris Commune. Address to the International Workingmen’s Association, May 1871......... 58
Endnotes........................................................................................................................................ 67
2 Introduction
Editorial Introduction
The “Manifesto of the Communist Party” was written by Marx and Engels as the Communist
League’s programme on the instruction of its Second Congress (London, November 29-December 8,
1847), which signified a victory for the followers of a new proletarian line during the discussion of the
programme questions.
When Congress was still in preparation, Marx and Engels arrived at the conclusion that the final
programme document should be in the form of a Party manifesto (see Engels’ letter to Marx of
November 23-24, 1847). The catechism form usual for the secret societies of the time and retained in
the “Draft of a Communist Confession of Faith” and “Principles of Communism,” was not suitable for
a full and substantial exposition of the new revolutionary world outlook, for a comprehensive
formulation of the proletarian movement’s aims and tasks. See also “Demands of the Communist
Party in Germany,” issued by Marx soon after publication of the Manifesto, which addressed the
immediate demands of the movement.
Marx and Engels began working together on the Manifesto while they were still in London
immediately after the congress, and continued until about December 13 when Marx returned to
Brussels; they resumed their work four days later (December 17) when Engels arrived there. After
Engels’ departure for Paris at the end of December and up to his return on January 31, Marx worked
on the Manifesto alone.
Hurried by the Central Authority of the Communist League which provided him with certain
documents (e.g., addresses of the People’s Chamber (Halle) of the League of the Just of November
1846 and February 1847, and, apparently, documents of the First Congress of the Communist League
pertaining to the discussion of the Party programme), Marx worked intensively on the Manifesto
through almost the whole of January 1848. At the end of January the manuscript was sent on to
London to be printed in the German Workers’ Educational Society’s print shop owned by a German
emigrant J. E. Burghard, a member of the Communist League.
The manuscript of the Manifesto has not survived. The only extant materials written in Marx’s hand
are a draft plan for Section III, showing his efforts to improve the structure of the Manifesto, and a
page of a rough copy.
The Manifesto came off the press at the end of February 1848. On February 29, the Educational
Society decided to cover all the printing expenses.
The first edition of the Manifesto was a 23-page pamphlet in a dark green cover. In April-May 1848
another edition was put out. The text took up 30 pages, some misprints of the first edition were
corrected, and the punctuation improved. Subsequently this text was used by Marx and Engels as a
basis for later authorised editions. Between March and July 1848 the Manifesto was printed in the
Deutsche Londoner Zeitung, a democratic newspaper of the German emigrants. Already that same
year numerous efforts were made to publish the Manifesto in other European languages. A Danish, a
Polish (in Paris) and a Swedish (under a different title: “The Voice of Communism. Declaration of the
Communist Party”) editions appeared in 1848. The translations into French, Italian and Spanish made
at that time remained unpublished. In April 1848, Engels, then in Barmen, was translating the
Manifesto into English, but he managed to translate only half of it, and the first English translation,
made by Helen Macfarlane, was not published until two years later, between June and November 1850,
in the Chartist journal The Red Republican. Its editor, Julian Harney, named the authors for the first
time in the introduction to this publication. All earlier and many subsequent editions of the Manifesto
were anonymous.
The growing emancipation struggle of the proletariat in the ’60s and ’70s of the 19th century led to
new editions of the Manifesto. The year 1872 saw a new German edition with minor corrections and a
preface by Marx and Engels where they drew some conclusions from the experience of the Paris 
3 Introduction
Commune of 1871. This and subsequent German editions (1883 and 1890) were entitled the
Communist Manifesto. In 1872 the Manifesto was first published in America in Woodhull & Claflin’s
Weekly.
The first Russian edition of the Manifesto, translated by Mikhail Bakunin with some distortions,
appeared in Geneva in 1869. The faults of this edition were removed in the 1882 edition (translation
by Georgi Plekhanov), for which Marx and Engels, who attributed great significance to the
dissemination of Marxism in Russia, had written a special preface.
After Marx’s death, the Manifesto ran into several editions. Engels read through them all, wrote
prefaces for the 1883 German edition and for the 1888 English edition in Samuel Moore’s translation,
which he also edited and supplied with notes. This edition served as a basis for many subsequent
editions of the Manifesto in English – in Britain, the United States and the USSR. In 1890, Engels
prepared a further German edition, wrote a new preface to it, and added a number of notes. In 1885,
the newspaper Le Socialiste published the French translation of the Manifesto made by Marx’s
daughter Laura Lafargue and read by Engels. He also wrote prefaces to the 1892 Polish and 1893
Italian editions.
This edition includes the two earlier versions of the Manifesto, namely the draft “Communist
Confession of Faith” and “The Principles of Communism,” both authored by Engels, as well as the
letter from Engels to Marx which poses the idea of publishing a “manifesto,” rather than a catechism.
The Manifesto addressed itself to a mass movement with historical significance, not a political sect.
On the other hand, the “Demands of the Communist Party in Germany” is included to place the
publication of the Manifesto in the context of the mass movement in Germany at the time, whose
immediate demands are reflected by Marx in this pamphlet. Clearly the aims of the Manifesto were
more far-reaching the movement in Germany at the time, and unlike the “Demands,” was intended to
outlive the immediate conditions.
The “Third Address to the International Workingmen’s Association” is included because in this
speech Marx examines the movement of the working class manifested in the Paris Commune, and his
observations here mark the only revisions to his social and historical vision made during his lifetime
as a result of the development of the working class movement itself, clarifying some points and
making others more concrete.
Preface to The 1872 German Edition
The Communist League, an international association of workers, which could of course be only a
secret one, under conditions obtaining at the time, commissioned us, the undersigned, at the
Congress held in London in November 1847, to write for publication a detailed theoretical and
practical programme for the Party. Such was the origin of the following Manifesto, the
manuscript of which travelled to London to be printed a few weeks before the February [French]
Revolution [in 1848]. First published in German, it has been republished in that language in at
least twelve different editions in Germany, England, and America. It was published in English for
the first time in 1850 in the Red Republican, London, translated by Miss Helen Macfarlane, and
in 1871 in at least three different translations in America. The French version first appeared in
Paris shortly before the June insurrection of 1848, and recently in Le Socialiste of New York. A
new translation is in the course of preparation. A Polish version appeared in London shortly after
it was first published in Germany. A Russian translation was published in Geneva in the sixties1
.
Into Danish, too, it was translated shortly after its appearance.
However much that state of things may have altered during the last twenty-five years, the general
principles laid down in the Manifesto are, on the whole, as correct today as ever. Here and there,
some detail might be improved. The practical application of the principles will depend, as the
Manifesto itself states, everywhere and at all times, on the historical conditions for the time being
existing, and, for that reason, no special stress is laid on the revolutionary measures proposed at
the end of Section II. That passage would, in many respects, be very differently worded today. In
view of the gigantic strides of Modern Industry since 1848, and of the accompanying improved
and extended organization of the working class, in view of the practical experience gained, first in
the February Revolution, and then, still more, in the Paris Commune, where the proletariat for the
first time held political power for two whole months, this programme has in some details been
antiquated. One thing especially was proved by the Commune, viz., that “the working class
cannot simply lay hold of the ready-made state machinery, and wield it for its own purposes.”
(See The Civil War in France: Address of the General Council of the International Working
Men’s Association, 1871, where this point is further developed.) Further, it is self-evident that the
criticism of socialist literature is deficient in relation to the present time, because it comes down
only to 1847; also that the remarks on the relation of the Communists to the various opposition
parties (Section IV), although, in principle still correct, yet in practice are antiquated, because the
political situation has been entirely changed, and the progress of history has swept from off the
earth the greater portion of the political parties there enumerated.
But then, the Manifesto has become a historical document which we have no longer any right to
alter. A subsequent edition may perhaps appear with an introduction bridging the gap from 1847
to the present day; but this reprint was too unexpected to leave us time for that.
Karl Marx & Frederick Engels
June 24, 1872, London
Preface to The 1882 Russian Edition
The first Russian edition of the Manifesto of the Communist Party, translated by Bakunin, was
published early in the ‘sixties by the printing office of the Kolokol [a reference to the Free
Russian Printing House]. Then the West could see in it (the Russian edition of the Manifesto)
only a literary curiosity. Such a view would be impossible today.
What a limited field the proletarian movement occupied at that time (December 1847) is most
clearly shown by the last section: the position of the Communists in relation to the various
opposition parties in various countries. Precisely Russia and the United States are missing here. It
was the time when Russia constituted the last great reserve of all European reaction, when the
United States absorbed the surplus proletarian forces of Europe through immigration. Both
countries provided Europe with raw materials and were at the same time markets for the sale of
its industrial products. Both were, therefore, in one way of another, pillars of the existing
European system.
How very different today. Precisely European immigration fitted North American for a gigantic
agricultural production, whose competition is shaking the very foundations of European landed
property – large and small. At the same time, it enabled the United States to exploit its
tremendous industrial resources with an energy and on a scale that must shortly break the
industrial monopoly of Western Europe, and especially of England, existing up to now. Both
circumstances react in a revolutionary manner upon America itself. Step by step, the small and
middle land ownership of the farmers, the basis of the whole political constitution, is succumbing
to the competition of giant farms; at the same time, a mass industrial proletariat and a fabulous
concentration of capital funds are developing for the first time in the industrial regions.
And now Russia! During the Revolution of 1848-9, not only the European princes, but the
European bourgeois as well, found their only salvation from the proletariat just beginning to
awaken in Russian intervention. The Tsar was proclaimed the chief of European reaction. Today,
he is a prisoner of war of the revolution in Gatchina 2
, and Russia forms the vanguard of
revolutionary action in Europe.
The Communist Manifesto had, as its object, the proclamation of the inevitable impending
dissolution of modern bourgeois property. But in Russia we find, face-to-face with the rapidly
flowering capitalist swindle and bourgeois property, just beginning to develop, more than half the
land owned in common by the peasants. Now the question is: can the Russian obshchina, though
greatly undermined, yet a form of primeval common ownership of land, pass directly to the
higher form of Communist common ownership? Or, on the contrary, must it first pass through the
same process of dissolution such as constitutes the historical evolution of the West?
The only answer to that possible today is this: If the Russian Revolution becomes the signal for a
proletarian revolution in the West, so that both complement each other, the present Russian
common ownership of land may serve as the starting point for a communist development.
Karl Marx & Frederick Engels
January 21, 1882, London
Preface to The 1883 German Edition
The preface to the present edition I must, alas, sign alone. Marx, the man to whom the whole
working class of Europe and America owes more than to any one else – rests at Highgate
Cemetery and over his grave the first grass is already growing. Since his death [March 14, 1883],
there can be even less thought of revising or supplementing the Manifesto. But I consider it all the
more necessary again to state the following expressly:
The basic thought running through the Manifesto – that economic production, and the structure of
society of every historical epoch necessarily arising therefrom, constitute the foundation for the
political and intellectual history of that epoch; that consequently (ever since the dissolution of the
primaeval communal ownership of land) all history has been a history of class struggles, of
struggles between exploited and exploiting, between dominated and dominating classes at various
stages of social evolution; that this struggle, however, has now reached a stage where the
exploited and oppressed class (the proletariat) can no longer emancipate itself from the class
which exploits and oppresses it (the bourgeoisie), without at the same time forever freeing the
whole of society from exploitation, oppression, class struggles – this basic thought belongs solely
and exclusively to Marx.*
I have already stated this many times; but precisely now is it necessary that it also stand in front
of the Manifesto itself.
Frederick Engels
June 28, 1883, London

* “This proposition,” I wrote in the preface to the English translation, “which, in my opinion, is destined to do for
history what Darwin’ s theory has done for biology, we both of us, had been gradually approaching for some years
before 1845. How far I had independently progressed towards it is best shown by my Conditions of the Working Class
in England. But when I again met Marx at Brussels, in spring 1845, he had it already worked out and put it before me
in terms almost as clear as those in which I have stated it here.” [Note by Engels to the German edition of 1890]
Preface to The 1888 English Edition
The Manifesto was published as the platform of the Communist League, a working men’ s
association, first exclusively German, later on international, and under the political conditions of
the Continent before 1848, unavoidably a secret society. At a Congress of the League, held in
November 1847, Marx and Engels were commissioned to prepare a complete theoretical and
practical party programme. Drawn up in German, in January 1848, the manuscript was sent to the
printer in London a few weeks before the French Revolution of February 24. A French translation
was brought out in Paris shortly before the insurrection of June 1848. The first English
translation, by Miss Helen Macfarlane, appeared in George Julian Harney’ s Red Republican,
London, 1850. A Danish and a Polish edition had also been published.
The defeat of the Parisian insurrection of June 1848 – the first great battle between proletariat and
bourgeoisie – drove again into the background, for a time, the social and political aspirations of
the European working class. Thenceforth, the struggle for supremacy was, again, as it had been
before the Revolution of February, solely between different sections of the propertied class; the
working class was reduced to a fight for political elbow-room, and to the position of extreme
wing of the middle-class Radicals. Wherever independent proletarian movements continued to
show signs of life, they were ruthlessly hunted down. Thus the Prussian police hunted out the
Central Board of the Communist League, then located in Cologne. The members were arrested
and, after eighteen months’ imprisonment, they were tried in October 1852. This celebrated
“Cologne Communist Trial” lasted from October 4 till November 12; seven of the prisoners were
sentenced to terms of imprisonment in a fortress, varying from three to six years. Immediately
after the sentence, the League was formally dissolved by the remaining members. As to the
Manifesto, it seemed henceforth doomed to oblivion.
When the European workers had recovered sufficient strength for another attack on the ruling
classes, the International Working Men’ s Association sprang up. But this association, formed
with the express aim of welding into one body the whole militant proletariat of Europe and
America, could not at once proclaim the principles laid down in the Manifesto. The International
was bound to have a programme broad enough to be acceptable to the English trade unions, to the
followers of Proudhon in France, Belgium, Italy, and Spain, and to the Lassalleans in Germany.*
Marx, who drew up this programme to the satisfaction of all parties, entirely trusted to the
intellectual development of the working class, which was sure to result from combined action and
mutual discussion. The very events and vicissitudes in the struggle against capital, the defeats
even more than the victories, could not help bringing home to men’ s minds the insufficiency of
their various favorite nostrums, and preparing the way for a more complete insight into the true
conditions for working-class emancipation. And Marx was right. The International, on its
breaking in 1874, left the workers quite different men from what it found them in 1864.
Proudhonism in France, Lassalleanism in Germany, were dying out, and even the conservative
English trade unions, though most of them had long since severed their connection with the
International, were gradually advancing towards that point at which, last year at Swansea, their
president [W. Bevan] could say in their name: “Continental socialism has lost its terror for us.” In
fact, the principles of the Manifesto had made considerable headway among the working men of
all countries.
 * Lassalle personally, to us, always acknowledged himself to be a disciple of Marx, and, as such, stood on the ground of
the Manifesto. But in his first public agitation, 1862-1864, he did not go beyond demanding co-operative workshops
supported by state credit. 
8 Preface to the 1888 English Edition
The Manifesto itself came thus to the front again. Since 1850, the German text had been reprinted
several times in Switzerland, England, and America. In 1872, it was translated into English in
New York, where the translation was published in Woorhull and Claflin’s Weekly. From this
English version, a French one was made in Le Socialiste of New York. Since then, at least two
more English translations, more or less mutilated, have been brought out in America, and one of
them has been reprinted in England. The first Russian translation, made by Bakunin, was
published at Herzen’ s Kolokol office in Geneva, about 1863; a second one, by the heroic Vera
Zasulich, also in Geneva, in 1882. A new Danish edition is to be found in Socialdemokratisk
Bibliothek, Copenhagen, 1885; a fresh French translation in Le Socialiste, Paris, 1886. From this
latter, a Spanish version was prepared and published in Madrid, 1886. The German reprints are
not to be counted; there have been twelve altogether at the least. An Armenian translation, which
was to be published in Constantinople some months ago, did not see the light, I am told, because
the publisher was afraid of bringing out a book with the name of Marx on it, while the translator
declined to call it his own production. Of further translations into other languages I have heard
but had not seen. Thus the history of the Manifesto reflects the history of the modern workingclass movement; at present, it is doubtless the most wide spread, the most international
production of all socialist literature, the common platform acknowledged by millions of working
men from Siberia to California.
Yet, when it was written, we could not have called it a socialist manifesto. By Socialists, in 1847,
were understood, on the one hand the adherents of the various Utopian systems: Owenites in
England, Fourierists in France, both of them already reduced to the position of mere sects, and
gradually dying out; on the other hand, the most multifarious social quacks who, by all manner of
tinkering, professed to redress, without any danger to capital and profit, all sorts of social
grievances, in both cases men outside the working-class movement, and looking rather to the
“educated” classes for support. Whatever portion of the working class had become convinced of
the insufficiency of mere political revolutions, and had proclaimed the necessity of total social
change, called itself Communist. It was a crude, rough-hewn, purely instinctive sort of
communism; still, it touched the cardinal point and was powerful enough amongst the working
class to produce the Utopian communism of Cabet in France, and of Weitling in Germany. Thus,
in 1847, socialism was a middle-class movement, communism a working-class movement.
Socialism was, on the Continent at least, “respectable”; communism was the very opposite. And
as our notion, from the very beginning, was that “the emancipation of the workers must be the act
of the working class itself,” there could be no doubt as to which of the two names we must take.
Moreover, we have, ever since, been far from repudiating it.
The Manifesto being our joint production, I consider myself bound to state that the fundamental
proposition which forms the nucleus belongs to Marx. That proposition is: That in every
historical epoch, the prevailing mode of economic production and exchange, and the social
organization necessarily following from it, form the basis upon which it is built up, and from that
which alone can be explained the political and intellectual history of that epoch; that consequently
the whole history of mankind (since the dissolution of primitive tribal society, holding land in
common ownership) has been a history of class struggles, contests between exploiting and
exploited, ruling and oppressed classes; That the history of these class struggles forms a series of
evolutions in which, nowadays, a stage has been reached where the exploited and oppressed class
– the proletariat – cannot attain its emancipation from the sway of the exploiting and ruling class
– the bourgeoisie – without, at the same time, and once and for all, emancipating society at large
from all exploitation, oppression, class distinction, and class struggles.
This proposition, which, in my opinion, is destined to do for history what Darwin’ s theory has
done for biology, we both of us, had been gradually approaching for some years before 1845.
How far I had independently progressed towards it is best shown by my “Conditions of the
Working Class in England.” But when I again met Marx at Brussels, in spring 1845, he had it 
9 Preface to the 1888 English Edition
already worked out and put it before me in terms almost as clear as those in which I have stated it
here.
From our joint preface to the German edition of 1872, I quote the following:
“However much that state of things may have altered during the last twenty-five
years, the general principles laid down in the Manifesto are, on the whole, as
correct today as ever. Here and there, some detail might be improved. The
practical application of the principles will depend, as the Manifesto itself states,
everywhere and at all times, on the historical conditions for the time being
existing, and, for that reason, no special stress is laid on the revolutionary
measures proposed at the end of Section II. That passage would, in many respects,
be very differently worded today. In view of the gigantic strides of Modern
Industry since 1848, and of the accompanying improved and extended
organization of the working class, in view of the practical experience gained, first
in the February Revolution, and then, still more, in the Paris Commune, where the
proletariat for the first time held political power for two whole months, this
programme has in some details been antiquated. One thing especially was proved
by the Commune, viz., that “the working class cannot simply lay hold of readymade state machinery, and wield it for its own purposes.” (See The Civil War in
France: Address of the General Council of the International Working Men’ s
Association 1871, where this point is further developed.) Further, it is self-evident
that the criticism of socialist literature is deficient in relation to the present time,
because it comes down only to 1847; also that the remarks on the relation of the
Communists to the various opposition parties (Section IV), although, in principle
still correct, yet in practice are antiquated, because the political situation has been
entirely changed, and the progress of history has swept from off the Earth the
greater portion of the political parties there enumerated.
“But then, the Manifesto has become a historical document which we have no
longer any right to alter.”
The present translation is by Mr Samuel Moore, the translator of the greater portion of Marx’ s
“Capital.” We have revised it in common, and I have added a few notes explanatory of historical
allusions.
Frederick Engels
January 30, 1888, London
Preface to The 1890 German Edition
Since [the first German preface of 1883] was written, a new German edition of the Manifesto has
again become necessary, and much has also happened to the Manifesto which should be recorded
here.
A second Russian translation – by Vera Zasulich – appeared in Geneva in 1882; the preface to
that edition was written by Marx and myself. Unfortunately, the original German manuscript has
gone astray; I must therefore retranslate from the Russian which will in no way improve the text.
It reads:
[Reprint of the 1882 Russian Edition ]
At about the same date, a new Polish version appeared in Geneva: Manifest Kommunistyczny.
Furthermore, a new Danish translation has appeared in the Socialdemokratisk Bibliothek,
Copenhagen, 1885. Unfortunately, it is not quite complete; certain essential passages, which seem
to have presented difficulties to the translator, have been omitted, and, in addition, there are signs
of carelessness here and there, which are all the more unpleasantly conspicuous since the
translation indicates that had the translator taken a little more pains, he would have done an
excellent piece of work.
A new French version appeared in 1886, in Le Socialiste of Paris; it is the best published to date.
From this latter, a Spanish version was published the same year in El Socialista of Madrid, and
then reissued in pamphlet form: Manifesto del Partido Communista por Carlos Marx y F. Engels,
Madrid, Administracion de El Socialista, Hernan Cortes 8.
As a matter of curiosity, I may mention that in 1887 the manuscript of an Armenian translation
was offered to a publisher in Constantinople. But the good man did not have the courage to
publish something bearing the name of Marx and suggested that the translator set down his own
name as author, which the latter however declined.
After one, and then another, of the more or less inaccurate American translations had been
repeatedly reprinted in England, an authentic version at last appeared in 1888. This was my friend
Samuel Moore, and we went through it together once more before it went to press. It is entitled:
Manifesto of the Communist Party, by Karl Marx and Frederick Engels. Authorized English
translation, edited and annotated by Frederick Engels, 1888, London, William Reeves, 185 Fleet
Street, E.C. I have added some of the notes of that edition to the present one.
The Manifesto has had a history of its own. Greeted with enthusiasm, at the time of its
appearance, by the not at all numerous vanguard of scientific socialism (as is proved by the
translations mentioned in the first place), it was soon forced into the background by the reaction
that began with the defeat of the Paris workers in June 1848, and was finally excommunicated
“by law” in the conviction of the Cologne Communists in November 1852. With the
disappearance from the public scene of the workers’ movement that had begun with the February
Revolution, the Manifesto too passed into the background.
When the European workers had again gathered sufficient strength for a new onslaught upon the
power of the ruling classes, the International Working Men’ s Association came into being. Its
aim was to weld together into one huge army the whole militant working class of Europe and
America. Therefore it could not set out from the principles laid down in the Manifesto. It was
bound to have a programme which would not shut the door on the English trade unions, the
French, Belgian, Italian, and Spanish Proudhonists, and the German Lassalleans. This programme
– the considerations underlying the Statutes of the International – was drawn up by Marx with a
master hand acknowledged even by the Bakunin and the anarchists. For the ultimate final triumph 
11 Preface to the 1890 German Edition
of the ideas set forth in the Manifesto, Marx relied solely upon the intellectual development of the
working class, as it necessarily has to ensue from united action and discussion. The events and
vicissitudes in the struggle against capital, the defeats even more than the successes, could not but
demonstrate to the fighters the inadequacy of their former universal panaceas, and make their
minds more receptive to a thorough understanding of the true conditions for working-class
emancipation. And Marx was right. The working class of 1874, at the dissolution of the
International, was altogether different from that of 1864, at its foundation. Proudhonism in the
Latin countries, and the specific Lassalleanism in Germany, were dying out; and even the ten
arch-conservative English trade unions were gradually approaching the point where, in 1887, the
chairman of their Swansea Congress could say in their name: “Continental socialism has lost its
terror for us.” Yet by 1887 continental socialism was almost exclusively the theory heralded in
the Manifesto. Thus, to a certain extent, the history of the Manifesto reflects the history of the
modern working-class movement since 1848. At present, it is doubtless the most widely
circulated, the most international product of all socialist literature, the common programme of
many millions of workers of all countries from Siberia to California.
Nevertheless, when it appeared, we could not have called it a socialist manifesto. In 1847, two
kinds of people were considered socialists. On the one hand were the adherents of the various
utopian systems, notably the Owenites in England and the Fourierists in France, both of whom, at
that date, had already dwindled to mere sects gradually dying out. On the other, the manifold
types of social quacks who wanted to eliminate social abuses through their various universal
panaceas and all kinds of patch-work, without hurting capital and profit in the least. In both cases,
people who stood outside the labor movement and who looked for support rather to the
“educated” classes. The section of the working class, however, which demanded a radical
reconstruction of society, convinced that mere political revolutions were not enough, then called
itself Communist. It was still a rough-hewn, only instinctive and frequently somewhat crude
communism. Yet, it was powerful enough to bring into being two systems of utopian communism
– in France, the “Icarian” communists of Cabet, and in Germany that of Weitling. Socialism in
1847 signified a bourgeois movement, communism a working-class movement. Socialism was,
on the Continent at least, quite respectable, whereas communism was the very opposite. And
since we were very decidedly of the opinion as early as then that “the emancipation of the
workers must be the task of the working class itself,” [from the General Rules of the
International] we could have no hesitation as to which of the two names we should choose. Nor
has it ever occurred to us to repudiate it.
“Working men of all countries, unite!” But few voices responded when we proclaimed these
words to the world 42 years ago, on the eve of the first Paris Revolution in which the proletariat
came out with the demands of its own. On September 28, 1864, however, the proletarians of most
of the Western European countries joined hands in the International Working Men’ s Association
of glorious memory. True, the International itself lived only nine years. But that the eternal union
of the proletarians of all countries created by it is still alive and lives stronger than ever, there is
no better witness than this day. Because today3
, as I write these lines, the European and American
proletariat is reviewing its fighting forces, mobilized for the first time, mobilized as one army,
under one flag, for one immediate aim: the standard eight-hour working day to be established by
legal enactment, as proclaimed by the Geneva Congress of the International in 1866, and again by
the Paris Workers’ Congress of 1889. And today’ s spectacle will open the eyes of the capitalists
and landlords of all countries to the fact that today the proletarians of all countries are united
indeed.
If only Marx were still by my side to see this with his own eyes!
Frederick Engels
May 1, 1890, London
Preface to The 1892 Polish Edition
The fact that a new Polish edition of the Communist Manifesto has become necessary gives rise
to various thoughts.
First of all, it is noteworthy that of late the Manifesto has become an index, as it were, of the
development of large-scale industry on the European continent. In proportion as large-scale
industry expands in a given country, the demand grows among the workers of that country for
enlightenment regarding their position as the working class in relation to the possessing classes,
the socialist movement spreads among them and the demand for the Manifesto increases. Thus,
not only the state of the labour movement but also the degree of development of large-scale
industry can be measured with fair accuracy in every country by the number of copies of the
Manifesto circulated in the language of that country.
Accordingly, the new Polish edition indicates a decided progress of Polish industry. And there
can be no doubt whatever that this progress since the previous edition published ten years ago has
actually taken place. Russian Poland, Congress Poland, has become the big industrial region of
the Russian Empire. Whereas Russian large-scale industry is scattered sporadically – a part round
the Gulf of Finland, another in the centre (Moscow and Vladimir), a third along the coasts of the
Black and Azov seas, and still others elsewhere – Polish industry has been packed into a
relatively small area and enjoys both the advantages and disadvantages arising from such
concentration. The competing Russian manufacturers acknowledged the advantages when they
demanded protective tariffs against Poland, in spit of their ardent desire to transform the Poles
into Russians. The disadvantages – for the Polish manufacturers and the Russian government –
are manifest in the rapid spread of socialist ideas among the Polish workers and in the growing
demand for the Manifesto.
But the rapid development of Polish industry, outstripping that of Russia, is in its turn a new
proof of the inexhaustible vitality of the Polish people and a new guarantee of its impending
national restoration. And the restoration of an independent and strong Poland is a matter which
concerns not only the Poles but all of us. A sincere international collaboration of the European
nations is possible only if each of these nations is fully autonomous in its own house. The
Revolution of 1848, which under the banner of the proletariat, after all, merely let the proletarian
fighters do the work of the bourgeoisie, also secured the independence of Italy, Germany and
Hungary through its testamentary executors, Louis Bonaparte and Bismarck; but Poland, which
since 1792 had done more for the Revolution than all these three together, was left to its own
resources when it succumbed in 1863 to a tenfold greater Russian force. The nobility could
neither maintain nor regain Polish independence; today, to the bourgeoisie, this independence is,
to say the last, immaterial. Nevertheless, it is a necessity for the harmonious collaboration of the
European nations. It can be gained only by the young Polish proletariat, and in its hands it is
secure. For the workers of all the rest of Europe need the independence of Poland just as much as
the Polish workers themselves.
F. Engels
London, February 10, 1892 
Preface to The 1893 Italian Edition
Publication of the Manifesto of the Communist Party coincided, one may say, with March 18,
1848, the day of the revolution in Milan and Berlin, which were armed uprisings of the two
nations situated in the centre, the one, of the continent of Europe, the other, of the Mediterranean;
two nations until then enfeebled by division and internal strife, and thus fallen under foreign
domination. While Italy was subject to the Emperor of Austria, Germany underwent the yoke, not
less effective though more indirect, of the Tsar of all the Russias. The consequences of March 18,
1848, freed both Italy and Germany from this disgrace; if from 1848 to 1871 these two great
nations were reconstituted and somehow again put on their own, it was as Karl Marx used to say,
because the men who suppressed the Revolution of 1848 were, nevertheless, its testamentary
executors in spite of themselves.
Everywhere that revolution was the work of the working class; it was the latter that built the
barricades and paid with its lifeblood. Only the Paris workers, in overthrowing the government,
had the very definite intention of overthrowing the bourgeois regime. But conscious though they
were of the fatal antagonism existing between their own class and the bourgeoisie, still, neither
the economic progress of the country nor the intellectual development of the mass of French
workers had as yet reached the stage which would have made a social reconstruction possible. In
the final analysis, therefore, the fruits of the revolution were reaped by the capitalist class. In the
other countries, in Italy, in Germany, in Austria, the workers, from the very outset, did nothing
but raise the bourgeoisie to power. But in any country the rule of the bourgeoisie is impossible
without national independence Therefore, the Revolution of 1848 had to bring in its train the
unity and autonomy of the nations that had lacked them up to then: Italy, Germany, Hungary.
Poland will follow in turn.
Thus, if the Revolution of 1848 was not a socialist revolution, it paved the way, prepared the
ground for the latter. Through the impetus given to large-scaled industry in all countries, the
bourgeois regime during the last forty-five years has everywhere created a numerous,
concentrated and powerful proletariat. It has thus raised, to use the language of the Manifesto, its
own grave-diggers. Without restoring autonomy and unity to each nation, it will be impossible to
achieve the international union of the proletariat, or the peaceful and intelligent co-operation of
these nations toward common aims. Just imagine joint international action by the Italian,
Hungarian, German, Polish and Russian workers under the political conditions preceding 1848!
The battles fought in 1848 were thus not fought in vain. Nor have the forty-five years separating
us from that revolutionary epoch passed to no purpose. The fruits are ripening, and all I wish is
that the publication of this Italian translation may augur as well for the victory of the Italian
proletariat as the publication of the original did for the international revolution.
The Manifesto does full justice to the revolutionary part played by capitalism in the past. The first
capitalist nation was Italy. The close of the feudal Middle Ages, and the opening of the modern
capitalist era are marked by a colossal figured: an Italian, Dante, both the last poet of the Middle
Ages and the first poet of modern times. Today, as in 1300, a new historical era is approaching.
Will Italy give us the new Dante, who will mark the hour of birth of this new, proletarian era?
Frederick Engels
London, February 1, 1893 
Manifesto of the Communist Party
A spectre is haunting Europe – the spectre of communism. All the powers of old Europe have
entered into a holy alliance to exorcise this spectre: Pope and Tsar, Metternich and Guizot,
French Radicals and German police-spies.
Where is the party in opposition that has not been decried as communistic by its opponents in
power? Where is the opposition that has not hurled back the branding reproach of communism,
against the more advanced opposition parties, as well as against its reactionary adversaries?
Two things result from this fact:
I. Communism is already acknowledged by all European powers to be itself a
power.
II. It is high time that Communists should openly, in the face of the whole world,
publish their views, their aims, their tendencies, and meet this nursery tale of the
Spectre of Communism with a manifesto of the party itself.
To this end, Communists of various nationalities have assembled in London and sketched the
following manifesto, to be published in the English, French, German, Italian, Flemish and Danish
languages.
I. Bourgeois and Proletarians*
The history of all hitherto existing society† is the history of class struggles.
Freeman and slave, patrician and plebeian, lord and serf, guild-master‡ and journeyman, in a
word, oppressor and oppressed, stood in constant opposition to one another, carried on an
uninterrupted, now hidden, now open fight, a fight that each time ended, either in a revolutionary
reconstitution of society at large, or in the common ruin of the contending classes.
In the earlier epochs of history, we find almost everywhere a complicated arrangement of society
into various orders, a manifold gradation of social rank. In ancient Rome we have patricians,
knights, plebeians, slaves; in the Middle Ages, feudal lords, vassals, guild-masters, journeymen,
apprentices, serfs; in almost all of these classes, again, subordinate gradations.
The modern bourgeois society that has sprouted from the ruins of feudal society has not done
away with class antagonisms. It has but established new classes, new conditions of oppression,
new forms of struggle in place of the old ones.
 * By bourgeoisie is meant the class of modern capitalists, owners of the means of social production and employers of
wage labour. By proletariat, the class of modern wage labourers who, having no means of production of their own, are
reduced to selling their labour power in order to live. [Engels, 1888 English edition]
† That is, all written history. In 1847, the pre-history of society, the social organisation existing previous to recorded
history, all but unknown. Since then, August von Haxthausen (1792-1866) discovered common ownership of land in
Russia, Georg Ludwig von Maurer proved it to be the social foundation from which all Teutonic races started in history,
and, by and by, village communities were found to be, or to have been, the primitive form of society everywhere from
India to Ireland. The inner organisation of this primitive communistic society was laid bare, in its typical form, by
Lewis Henry Morgan's (1818-1861) crowning discovery of the true nature of the gens and its relation to the tribe. With
the dissolution of the primeval communities, society begins to be differentiated into separate and finally antagonistic
classes. I have attempted to retrace this dissolution in The Origin of the Family, Private Property, and the State, second
edition, Stuttgart, 1886. [Engels, 1888 English Edition and 1890 German Edition (with the last sentence omitted)]
‡ Guild-master, that is, a full member of a guild, a master within, not a head of a guild. [Engels, 1888 English Edition] 
15 Manifesto of the Communist Party
Our epoch, the epoch of the bourgeoisie, possesses, however, this distinct feature: it has
simplified class antagonisms. Society as a whole is more and more splitting up into two great
hostile camps, into two great classes directly facing each other – Bourgeoisie and Proletariat.
From the serfs of the Middle Ages sprang the chartered burghers of the earliest towns. From these
burgesses the first elements of the bourgeoisie were developed.
The discovery of America, the rounding of the Cape, opened up fresh ground for the rising
bourgeoisie. The East-Indian and Chinese markets, the colonisation of America, trade with the
colonies, the increase in the means of exchange and in commodities generally, gave to commerce,
to navigation, to industry, an impulse never before known, and thereby, to the revolutionary
element in the tottering feudal society, a rapid development.
The feudal system of industry, in which industrial production was monopolised by closed guilds,
now no longer sufficed for the growing wants of the new markets. The manufacturing system
took its place. The guild-masters were pushed on one side by the manufacturing middle class;
division of labour between the different corporate guilds vanished in the face of division of labour
in each single workshop.
Meantime the markets kept ever growing, the demand ever rising. Even manufacturer no longer
sufficed. Thereupon, steam and machinery revolutionised industrial production. The place of
manufacture was taken by the giant, Modern Industry; the place of the industrial middle class by
industrial millionaires, the leaders of the whole industrial armies, the modern bourgeois.
Modern industry has established the world market, for which the discovery of America paved the
way. This market has given an immense development to commerce, to navigation, to
communication by land. This development has, in its turn, reacted on the extension of industry;
and in proportion as industry, commerce, navigation, railways extended, in the same proportion
the bourgeoisie developed, increased its capital, and pushed into the background every class
handed down from the Middle Ages.
We see, therefore, how the modern bourgeoisie is itself the product of a long course of
development, of a series of revolutions in the modes of production and of exchange.
Each step in the development of the bourgeoisie was accompanied by a corresponding political
advance of that class. An oppressed class under the sway of the feudal nobility, an armed and
self-governing association in the medieval commune*
: here independent urban republic (as in
Italy and Germany); there taxable “third estate” of the monarchy (as in France); afterwards, in the
period of manufacturing proper, serving either the semi-feudal or the absolute monarchy as a
counterpoise against the nobility, and, in fact, cornerstone of the great monarchies in general, the
bourgeoisie has at last, since the establishment of Modern Industry and of the world market,
conquered for itself, in the modern representative State, exclusive political sway. The executive
of the modern state is but a committee for managing the common affairs of the whole
bourgeoisie.
The bourgeoisie, historically, has played a most revolutionary part.
The bourgeoisie, wherever it has got the upper hand, has put an end to all feudal, patriarchal,
idyllic relations. It has pitilessly torn asunder the motley feudal ties that bound man to his
“natural superiors”, and has left remaining no other nexus between man and man than naked selfinterest, than callous “cash payment”. It has drowned the most heavenly ecstasies of religious
 * This was the name given their urban communities by the townsmen of Italy and France, after they had purchased or
conquered their initial rights of self-government from their feudal lords. [Engels, 1890 German edition] “Commune”
was the name taken in France by the nascent towns even before they had conquered from their feudal lords and masters
local self-government and political rights as the “Third Estate.” Generally speaking, for the economical development of
the bourgeoisie, England is here taken as the typical country, for its political development, France. [Engels, 1888
English Edition]
16 Manifesto of the Communist Party
fervour, of chivalrous enthusiasm, of philistine sentimentalism, in the icy water of egotistical
calculation. It has resolved personal worth into exchange value, and in place of the numberless
indefeasible chartered freedoms, has set up that single, unconscionable freedom – Free Trade. In
one word, for exploitation, veiled by religious and political illusions, it has substituted naked,
shameless, direct, brutal exploitation.
The bourgeoisie has stripped of its halo every occupation hitherto honoured and looked up to with
reverent awe. It has converted the physician, the lawyer, the priest, the poet, the man of science,
into its paid wage labourers.
The bourgeoisie has torn away from the family its sentimental veil, and has reduced the family
relation to a mere money relation.
The bourgeoisie has disclosed how it came to pass that the brutal display of vigour in the Middle
Ages, which reactionaries so much admire, found its fitting complement in the most slothful
indolence. It has been the first to show what man’s activity can bring about. It has accomplished
wonders far surpassing Egyptian pyramids, Roman aqueducts, and Gothic cathedrals; it has
conducted expeditions that put in the shade all former Exoduses of nations and crusades.
The bourgeoisie cannot exist without constantly revolutionising the instruments of production,
and thereby the relations of production, and with them the whole relations of society.
Conservation of the old modes of production in unaltered form, was, on the contrary, the first
condition of existence for all earlier industrial classes. Constant revolutionising of production,
uninterrupted disturbance of all social conditions, everlasting uncertainty and agitation
distinguish the bourgeois epoch from all earlier ones. All fixed, fast-frozen relations, with their
train of ancient and venerable prejudices and opinions, are swept away, all new-formed ones
become antiquated before they can ossify. All that is solid melts into air, all that is holy is
profaned, and man is at last compelled to face with sober senses his real conditions of life, and his
relations with his kind.
The need of a constantly expanding market for its products chases the bourgeoisie over the entire
surface of the globe. It must nestle everywhere, settle everywhere, establish connexions
everywhere.
The bourgeoisie has through its exploitation of the world market given a cosmopolitan character
to production and consumption in every country. To the great chagrin of Reactionists, it has
drawn from under the feet of industry the national ground on which it stood. All old-established
national industries have been destroyed or are daily being destroyed. They are dislodged by new
industries, whose introduction becomes a life and death question for all civilised nations, by
industries that no longer work up indigenous raw material, but raw material drawn from the
remotest zones; industries whose products are consumed, not only at home, but in every quarter
of the globe. In place of the old wants, satisfied by the production of the country, we find new
wants, requiring for their satisfaction the products of distant lands and climes. In place of the old
local and national seclusion and self-sufficiency, we have intercourse in every direction, universal
inter-dependence of nations. And as in material, so also in intellectual production. The intellectual
creations of individual nations become common property. National one-sidedness and narrowmindedness become more and more impossible, and from the numerous national and local
literatures, there arises a world literature.
The bourgeoisie, by the rapid improvement of all instruments of production, by the immensely
facilitated means of communication, draws all, even the most barbarian, nations into civilisation.
The cheap prices of commodities are the heavy artillery with which it batters down all Chinese
walls, with which it forces the barbarians’ intensely obstinate hatred of foreigners to capitulate. It
compels all nations, on pain of extinction, to adopt the bourgeois mode of production; it compels
them to introduce what it calls civilisation into their midst, i.e., to become bourgeois themselves.
In one word, it creates a world after its own image. 
17 Manifesto of the Communist Party
The bourgeoisie has subjected the country to the rule of the towns. It has created enormous cities,
has greatly increased the urban population as compared with the rural, and has thus rescued a
considerable part of the population from the idiocy of rural life. Just as it has made the country
dependent on the towns, so it has made barbarian and semi-barbarian countries dependent on the
civilised ones, nations of peasants on nations of bourgeois, the East on the West.
The bourgeoisie keeps more and more doing away with the scattered state of the population, of
the means of production, and of property. It has agglomerated population, centralised the means
of production, and has concentrated property in a few hands. The necessary consequence of this
was political centralisation. Independent, or but loosely connected provinces, with separate
interests, laws, governments, and systems of taxation, became lumped together into one nation,
with one government, one code of laws, one national class-interest, one frontier, and one
customs-tariff.
The bourgeoisie, during its rule of scarce one hundred years, has created more massive and more
colossal productive forces than have all preceding generations together. Subjection of Nature’s
forces to man, machinery, application of chemistry to industry and agriculture, steam-navigation,
railways, electric telegraphs, clearing of whole continents for cultivation, canalisation of rivers,
whole populations conjured out of the ground – what earlier century had even a presentiment that
such productive forces slumbered in the lap of social labour?
We see then: the means of production and of exchange, on whose foundation the bourgeoisie built
itself up, were generated in feudal society. At a certain stage in the development of these means
of production and of exchange, the conditions under which feudal society produced and
exchanged, the feudal organisation of agriculture and manufacturing industry, in one word, the
feudal relations of property became no longer compatible with the already developed productive
forces; they became so many fetters. They had to be burst asunder; they were burst asunder.
Into their place stepped free competition, accompanied by a social and political constitution
adapted in it, and the economic and political sway of the bourgeois class.
A similar movement is going on before our own eyes. Modern bourgeois society, with its
relations of production, of exchange and of property, a society that has conjured up such gigantic
means of production and of exchange, is like the sorcerer who is no longer able to control the
powers of the nether world whom he has called up by his spells. For many a decade past the
history of industry and commerce is but the history of the revolt of modern productive forces
against modern conditions of production, against the property relations that are the conditions for
the existence of the bourgeois and of its rule. It is enough to mention the commercial crises that
by their periodical return put the existence of the entire bourgeois society on its trial, each time
more threateningly. In these crises, a great part not only of the existing products, but also of the
previously created productive forces, are periodically destroyed. In these crises, there breaks out
an epidemic that, in all earlier epochs, would have seemed an absurdity – the epidemic of overproduction. Society suddenly finds itself put back into a state of momentary barbarism; it appears
as if a famine, a universal war of devastation, had cut off the supply of every means of
subsistence; industry and commerce seem to be destroyed; and why? Because there is too much
civilisation, too much means of subsistence, too much industry, too much commerce. The
productive forces at the disposal of society no longer tend to further the development of the
conditions of bourgeois property; on the contrary, they have become too powerful for these
conditions, by which they are fettered, and so soon as they overcome these fetters, they bring
disorder into the whole of bourgeois society, endanger the existence of bourgeois property. The
conditions of bourgeois society are too narrow to comprise the wealth created by them. And how
does the bourgeoisie get over these crises? On the one hand by enforced destruction of a mass of
productive forces; on the other, by the conquest of new markets, and by the more thorough
exploitation of the old ones. That is to say, by paving the way for more extensive and more
destructive crises, and by diminishing the means whereby crises are prevented. 
18 Manifesto of the Communist Party
The weapons with which the bourgeoisie felled feudalism to the ground are now turned against
the bourgeoisie itself.
But not only has the bourgeoisie forged the weapons that bring death to itself; it has also called
into existence the men who are to wield those weapons – the modern working class – the
proletarians.
In proportion as the bourgeoisie, i.e., capital, is developed, in the same proportion is the
proletariat, the modern working class, developed – a class of labourers, who live only so long as
they find work, and who find work only so long as their labour increases capital. These labourers,
who must sell themselves piecemeal, are a commodity, like every other article of commerce, and
are consequently exposed to all the vicissitudes of competition, to all the fluctuations of the
market.
Owing to the extensive use of machinery, and to the division of labour, the work of the
proletarians has lost all individual character, and, consequently, all charm for the workman. He
becomes an appendage of the machine, and it is only the most simple, most monotonous, and
most easily acquired knack, that is required of him. Hence, the cost of production of a workman is
restricted, almost entirely, to the means of subsistence that he requires for maintenance, and for
the propagation of his race. But the price of a commodity, and therefore also of labour, is equal to
its cost of production. In proportion, therefore, as the repulsiveness of the work increases, the
wage decreases. Nay more, in proportion as the use of machinery and division of labour
increases, in the same proportion the burden of toil also increases, whether by prolongation of the
working hours, by the increase of the work exacted in a given time or by increased speed of
machinery, etc.
Modern Industry has converted the little workshop of the patriarchal master into the great factory
of the industrial capitalist. Masses of labourers, crowded into the factory, are organised like
soldiers. As privates of the industrial army they are placed under the command of a perfect
hierarchy of officers and sergeants. Not only are they slaves of the bourgeois class, and of the
bourgeois State; they are daily and hourly enslaved by the machine, by the overlooker, and, above
all, by the individual bourgeois manufacturer himself. The more openly this despotism proclaims
gain to be its end and aim, the more petty, the more hateful and the more embittering it is.
The less the skill and exertion of strength implied in manual labour, in other words, the more
modern industry becomes developed, the more is the labour of men superseded by that of women.
Differences of age and sex have no longer any distinctive social validity for the working class.
All are instruments of labour, more or less expensive to use, according to their age and sex.
No sooner is the exploitation of the labourer by the manufacturer, so far, at an end, that he
receives his wages in cash, than he is set upon by the other portions of the bourgeoisie, the
landlord, the shopkeeper, the pawnbroker, etc.
The lower strata of the middle class – the small tradespeople, shopkeepers, and retired tradesmen
generally, the handicraftsmen and peasants – all these sink gradually into the proletariat, partly
because their diminutive capital does not suffice for the scale on which Modern Industry is
carried on, and is swamped in the competition with the large capitalists, partly because their
specialised skill is rendered worthless by new methods of production. Thus the proletariat is
recruited from all classes of the population.
The proletariat goes through various stages of development. With its birth begins its struggle with
the bourgeoisie. At first the contest is carried on by individual labourers, then by the workpeople
of a factory, then by the operative of one trade, in one locality, against the individual bourgeois
who directly exploits them. They direct their attacks not against the bourgeois conditions of
production, but against the instruments of production themselves; they destroy imported wares
that compete with their labour, they smash to pieces machinery, they set factories ablaze, they
seek to restore by force the vanished status of the workman of the Middle Ages. 
19 Manifesto of the Communist Party
At this stage, the labourers still form an incoherent mass scattered over the whole country, and
broken up by their mutual competition. If anywhere they unite to form more compact bodies, this
is not yet the consequence of their own active union, but of the union of the bourgeoisie, which
class, in order to attain its own political ends, is compelled to set the whole proletariat in motion,
and is moreover yet, for a time, able to do so. At this stage, therefore, the proletarians do not fight
their enemies, but the enemies of their enemies, the remnants of absolute monarchy, the
landowners, the non-industrial bourgeois, the petty bourgeois. Thus, the whole historical
movement is concentrated in the hands of the bourgeoisie; every victory so obtained is a victory
for the bourgeoisie.
But with the development of industry, the proletariat not only increases in number; it becomes
concentrated in greater masses, its strength grows, and it feels that strength more. The various
interests and conditions of life within the ranks of the proletariat are more and more equalised, in
proportion as machinery obliterates all distinctions of labour, and nearly everywhere reduces
wages to the same low level. The growing competition among the bourgeois, and the resulting
commercial crises, make the wages of the workers ever more fluctuating. The increasing
improvement of machinery, ever more rapidly developing, makes their livelihood more and more
precarious; the collisions between individual workmen and individual bourgeois take more and
more the character of collisions between two classes. Thereupon, the workers begin to form
combinations (Trades’ Unions) against the bourgeois; they club together in order to keep up the
rate of wages; they found permanent associations in order to make provision beforehand for these
occasional revolts. Here and there, the contest breaks out into riots.
Now and then the workers are victorious, but only for a time. The real fruit of their battles lies,
not in the immediate result, but in the ever expanding union of the workers. This union is helped
on by the improved means of communication that are created by modern industry, and that place
the workers of different localities in contact with one another. It was just this contact that was
needed to centralise the numerous local struggles, all of the same character, into one national
struggle between classes. But every class struggle is a political struggle. And that union, to attain
which the burghers of the Middle Ages, with their miserable highways, required centuries, the
modern proletarian, thanks to railways, achieve in a few years.
This organisation of the proletarians into a class, and, consequently into a political party, is
continually being upset again by the competition between the workers themselves. But it ever
rises up again, stronger, firmer, mightier. It compels legislative recognition of particular interests
of the workers, by taking advantage of the divisions among the bourgeoisie itself. Thus, the tenhours’ bill in England was carried.
Altogether collisions between the classes of the old society further, in many ways, the course of
development of the proletariat. The bourgeoisie finds itself involved in a constant battle. At first
with the aristocracy; later on, with those portions of the bourgeoisie itself, whose interests have
become antagonistic to the progress of industry; at all time with the bourgeoisie of foreign
countries. In all these battles, it sees itself compelled to appeal to the proletariat, to ask for help,
and thus, to drag it into the political arena. The bourgeoisie itself, therefore, supplies the
proletariat with its own elements of political and general education, in other words, it furnishes
the proletariat with weapons for fighting the bourgeoisie.
Further, as we have already seen, entire sections of the ruling class are, by the advance of
industry, precipitated into the proletariat, or are at least threatened in their conditions of existence.
These also supply the proletariat with fresh elements of enlightenment and progress.
Finally, in times when the class struggle nears the decisive hour, the progress of dissolution going
on within the ruling class, in fact within the whole range of old society, assumes such a violent,
glaring character, that a small section of the ruling class cuts itself adrift, and joins the
revolutionary class, the class that holds the future in its hands. Just as, therefore, at an earlier 
20 Manifesto of the Communist Party
period, a section of the nobility went over to the bourgeoisie, so now a portion of the bourgeoisie
goes over to the proletariat, and in particular, a portion of the bourgeois ideologists, who have
raised themselves to the level of comprehending theoretically the historical movement as a whole.
Of all the classes that stand face to face with the bourgeoisie today, the proletariat alone is a
really revolutionary class. The other classes decay and finally disappear in the face of Modern
Industry; the proletariat is its special and essential product.
The lower middle class, the small manufacturer, the shopkeeper, the artisan, the peasant, all these
fight against the bourgeoisie, to save from extinction their existence as fractions of the middle
class. They are therefore not revolutionary, but conservative. Nay more, they are reactionary, for
they try to roll back the wheel of history. If by chance, they are revolutionary, they are only so in
view of their impending transfer into the proletariat; they thus defend not their present, but their
future interests, they desert their own standpoint to place themselves at that of the proletariat.
The “dangerous class”, [lumpenproletariat] the social scum, that passively rotting mass thrown
off by the lowest layers of the old society, may, here and there, be swept into the movement by a
proletarian revolution; its conditions of life, however, prepare it far more for the part of a bribed
tool of reactionary intrigue.
In the condition of the proletariat, those of old society at large are already virtually swamped. The
proletarian is without property; his relation to his wife and children has no longer anything in
common with the bourgeois family relations; modern industry labour, modern subjection to
capital, the same in England as in France, in America as in Germany, has stripped him of every
trace of national character. Law, morality, religion, are to him so many bourgeois prejudices,
behind which lurk in ambush just as many bourgeois interests.
All the preceding classes that got the upper hand sought to fortify their already acquired status by
subjecting society at large to their conditions of appropriation. The proletarians cannot become
masters of the productive forces of society, except by abolishing their own previous mode of
appropriation, and thereby also every other previous mode of appropriation. They have nothing of
their own to secure and to fortify; their mission is to destroy all previous securities for, and
insurances of, individual property.
All previous historical movements were movements of minorities, or in the interest of minorities.
The proletarian movement is the self-conscious, independent movement of the immense majority,
in the interest of the immense majority. The proletariat, the lowest stratum of our present society,
cannot stir, cannot raise itself up, without the whole superincumbent strata of official society
being sprung into the air.
Though not in substance, yet in form, the struggle of the proletariat with the bourgeoisie is at first
a national struggle. The proletariat of each country must, of course, first of all settle matters with
its own bourgeoisie.
In depicting the most general phases of the development of the proletariat, we traced the more or
less veiled civil war, raging within existing society, up to the point where that war breaks out into
open revolution, and where the violent overthrow of the bourgeoisie lays the foundation for the
sway of the proletariat.
Hitherto, every form of society has been based, as we have already seen, on the antagonism of
oppressing and oppressed classes. But in order to oppress a class, certain conditions must be
assured to it under which it can, at least, continue its slavish existence. The serf, in the period of
serfdom, raised himself to membership in the commune, just as the petty bourgeois, under the
yoke of the feudal absolutism, managed to develop into a bourgeois. The modern labourer, on the
contrary, instead of rising with the process of industry, sinks deeper and deeper below the
conditions of existence of his own class. He becomes a pauper, and pauperism develops more
rapidly than population and wealth. And here it becomes evident, that the bourgeoisie is unfit any
longer to be the ruling class in society, and to impose its conditions of existence upon society as 
21 Manifesto of the Communist Party
an over-riding law. It is unfit to rule because it is incompetent to assure an existence to its slave
within his slavery, because it cannot help letting him sink into such a state, that it has to feed him,
instead of being fed by him. Society can no longer live under this bourgeoisie, in other words, its
existence is no longer compatible with society.
The essential conditions for the existence and for the sway of the bourgeois class is the formation
and augmentation of capital; the condition for capital is wage-labour. Wage-labour rests
exclusively on competition between the labourers. The advance of industry, whose involuntary
promoter is the bourgeoisie, replaces the isolation of the labourers, due to competition, by the
revolutionary combination, due to association. The development of Modern Industry, therefore,
cuts from under its feet the very foundation on which the bourgeoisie produces and appropriates
products. What the bourgeoisie therefore produces, above all, are its own grave-diggers. Its fall
and the victory of the proletariat are equally inevitable. 
II. Proletarians and Communists
In what relation do the Communists stand to the proletarians as a whole?
The Communists do not form a separate party opposed to the other working-class parties.
They have no interests separate and apart from those of the proletariat as a whole.
They do not set up any sectarian principles of their own, by which to shape and mould the
proletarian movement.
The Communists are distinguished from the other working-class parties by this only: 1. In the
national struggles of the proletarians of the different countries, they point out and bring to the
front the common interests of the entire proletariat, independently of all nationality. 2. In the
various stages of development which the struggle of the working class against the bourgeoisie has
to pass through, they always and everywhere represent the interests of the movement as a whole.
The Communists, therefore, are on the one hand, practically, the most advanced and resolute
section of the working-class parties of every country, that section which pushes forward all
others; on the other hand, theoretically, they have over the great mass of the proletariat the
advantage of clearly understanding the line of march, the conditions, and the ultimate general
results of the proletarian movement.
The immediate aim of the Communists is the same as that of all other proletarian parties:
formation of the proletariat into a class, overthrow of the bourgeois supremacy, conquest of
political power by the proletariat.
The theoretical conclusions of the Communists are in no way based on ideas or principles that
have been invented, or discovered, by this or that would-be universal reformer.
They merely express, in general terms, actual relations springing from an existing class struggle,
from a historical movement going on under our very eyes. The abolition of existing property
relations is not at all a distinctive feature of communism.
All property relations in the past have continually been subject to historical change consequent
upon the change in historical conditions.
The French Revolution, for example, abolished feudal property in favour of bourgeois property.
The distinguishing feature of Communism is not the abolition of property generally, but the
abolition of bourgeois property. But modern bourgeois private property is the final and most
complete expression of the system of producing and appropriating products, that is based on class
antagonisms, on the exploitation of the many by the few.
In this sense, the theory of the Communists may be summed up in the single sentence: Abolition
of private property.
We Communists have been reproached with the desire of abolishing the right of personally
acquiring property as the fruit of a man’s own labour, which property is alleged to be the
groundwork of all personal freedom, activity and independence.
Hard-won, self-acquired, self-earned property! Do you mean the property of petty artisan and of
the small peasant, a form of property that preceded the bourgeois form? There is no need to
abolish that; the development of industry has to a great extent already destroyed it, and is still
destroying it daily.
Or do you mean the modern bourgeois private property?
But does wage-labour create any property for the labourer? Not a bit. It creates capital, i.e., that
kind of property which exploits wage-labour, and which cannot increase except upon condition of
begetting a new supply of wage-labour for fresh exploitation. Property, in its present form, is 
23 Chapter II: Proletarians and Communists
based on the antagonism of capital and wage labour. Let us examine both sides of this
antagonism.
To be a capitalist, is to have not only a purely personal, but a social status in production. Capital
is a collective product, and only by the united action of many members, nay, in the last resort,
only by the united action of all members of society, can it be set in motion.
Capital is therefore not only personal; it is a social power.
When, therefore, capital is converted into common property, into the property of all members of
society, personal property is not thereby transformed into social property. It is only the social
character of the property that is changed. It loses its class character.
Let us now take wage-labour.
The average price of wage-labour is the minimum wage, i.e., that quantum of the means of
subsistence which is absolutely requisite to keep the labourer in bare existence as a labourer.
What, therefore, the wage-labourer appropriates by means of his labour, merely suffices to
prolong and reproduce a bare existence. We by no means intend to abolish this personal
appropriation of the products of labour, an appropriation that is made for the maintenance and
reproduction of human life, and that leaves no surplus wherewith to command the labour of
others. All that we want to do away with is the miserable character of this appropriation, under
which the labourer lives merely to increase capital, and is allowed to live only in so far as the
interest of the ruling class requires it.
In bourgeois society, living labour is but a means to increase accumulated labour. In Communist
society, accumulated labour is but a means to widen, to enrich, to promote the existence of the
labourer.
In bourgeois society, therefore, the past dominates the present; in Communist society, the present
dominates the past. In bourgeois society capital is independent and has individuality, while the
living person is dependent and has no individuality.
And the abolition of this state of things is called by the bourgeois, abolition of individuality and
freedom! And rightly so. The abolition of bourgeois individuality, bourgeois independence, and
bourgeois freedom is undoubtedly aimed at.
By freedom is meant, under the present bourgeois conditions of production, free trade, free
selling and buying.
But if selling and buying disappears, free selling and buying disappears also. This talk about free
selling and buying, and all the other “brave words” of our bourgeois about freedom in general,
have a meaning, if any, only in contrast with restricted selling and buying, with the fettered
traders of the Middle Ages, but have no meaning when opposed to the Communistic abolition of
buying and selling, of the bourgeois conditions of production, and of the bourgeoisie itself.
You are horrified at our intending to do away with private property. But in your existing society,
private property is already done away with for nine-tenths of the population; its existence for the
few is solely due to its non-existence in the hands of those nine-tenths. You reproach us,
therefore, with intending to do away with a form of property, the necessary condition for whose
existence is the non-existence of any property for the immense majority of society.
In one word, you reproach us with intending to do away with your property. Precisely so; that is
just what we intend.
From the moment when labour can no longer be converted into capital, money, or rent, into a
social power capable of being monopolised, i.e., from the moment when individual property can
no longer be transformed into bourgeois property, into capital, from that moment, you say,
individuality vanishes. 
24 Chapter II: Proletarians and Communists
You must, therefore, confess that by “individual” you mean no other person than the bourgeois,
than the middle-class owner of property. This person must, indeed, be swept out of the way, and
made impossible.
Communism deprives no man of the power to appropriate the products of society; all that it does
is to deprive him of the power to subjugate the labour of others by means of such appropriations.
It has been objected that upon the abolition of private property, all work will cease, and universal
laziness will overtake us.
According to this, bourgeois society ought long ago to have gone to the dogs through sheer
idleness; for those of its members who work, acquire nothing, and those who acquire anything do
not work. The whole of this objection is but another expression of the tautology: that there can no
longer be any wage-labour when there is no longer any capital.
All objections urged against the Communistic mode of producing and appropriating material
products, have, in the same way, been urged against the Communistic mode of producing and
appropriating intellectual products. Just as, to the bourgeois, the disappearance of class property
is the disappearance of production itself, so the disappearance of class culture is to him identical
with the disappearance of all culture.
That culture, the loss of which he laments, is, for the enormous majority, a mere training to act as
a machine.
But don’t wrangle with us so long as you apply, to our intended abolition of bourgeois property,
the standard of your bourgeois notions of freedom, culture, law, &c. Your very ideas are but the
outgrowth of the conditions of your bourgeois production and bourgeois property, just as your
jurisprudence is but the will of your class made into a law for all, a will whose essential character
and direction are determined by the economical conditions of existence of your class.
The selfish misconception that induces you to transform into eternal laws of nature and of reason,
the social forms springing from your present mode of production and form of property –
historical relations that rise and disappear in the progress of production – this misconception you
share with every ruling class that has preceded you. What you see clearly in the case of ancient
property, what you admit in the case of feudal property, you are of course forbidden to admit in
the case of your own bourgeois form of property.
Abolition [Aufhebung] of the family! Even the most radical flare up at this infamous proposal of
the Communists.
On what foundation is the present family, the bourgeois family, based? On capital, on private
gain. In its completely developed form, this family exists only among the bourgeoisie. But this
state of things finds its complement in the practical absence of the family among the proletarians,
and in public prostitution.
The bourgeois family will vanish as a matter of course when its complement vanishes, and both
will vanish with the vanishing of capital.
Do you charge us with wanting to stop the exploitation of children by their parents? To this crime
we plead guilty.
But, you say, we destroy the most hallowed of relations, when we replace home education by
social.
And your education! Is not that also social, and determined by the social conditions under which
you educate, by the intervention direct or indirect, of society, by means of schools, &c.? The
Communists have not invented the intervention of society in education; they do but seek to alter
the character of that intervention, and to rescue education from the influence of the ruling class.
The bourgeois clap-trap about the family and education, about the hallowed co-relation of parents
and child, becomes all the more disgusting, the more, by the action of Modern Industry, all the 
25 Chapter II: Proletarians and Communists
family ties among the proletarians are torn asunder, and their children transformed into simple
articles of commerce and instruments of labour.
But you Communists would introduce community of women, screams the bourgeoisie in chorus.
The bourgeois sees his wife a mere instrument of production. He hears that the instruments of
production are to be exploited in common, and, naturally, can come to no other conclusion that
the lot of being common to all will likewise fall to the women.
He has not even a suspicion that the real point aimed at is to do away with the status of women as
mere instruments of production.
For the rest, nothing is more ridiculous than the virtuous indignation of our bourgeois at the
community of women which, they pretend, is to be openly and officially established by the
Communists. The Communists have no need to introduce community of women; it has existed
almost from time immemorial.
Our bourgeois, not content with having wives and daughters of their proletarians at their disposal,
not to speak of common prostitutes, take the greatest pleasure in seducing each other’s wives.
Bourgeois marriage is, in reality, a system of wives in common and thus, at the most, what the
Communists might possibly be reproached with is that they desire to introduce, in substitution for
a hypocritically concealed, an openly legalised community of women. For the rest, it is selfevident that the abolition of the present system of production must bring with it the abolition of
the community of women springing from that system, i.e., of prostitution both public and private.
The Communists are further reproached with desiring to abolish countries and nationality.
The working men have no country. We cannot take from them what they have not got. Since the
proletariat must first of all acquire political supremacy, must rise to be the leading class of the
nation, must constitute itself the nation, it is so far, itself national, though not in the bourgeois
sense of the word.
National differences and antagonism between peoples are daily more and more vanishing, owing
to the development of the bourgeoisie, to freedom of commerce, to the world market, to
uniformity in the mode of production and in the conditions of life corresponding thereto.
The supremacy of the proletariat will cause them to vanish still faster. United action, of the
leading civilised countries at least, is one of the first conditions for the emancipation of the
proletariat.
In proportion as the exploitation of one individual by another will also be put an end to, the
exploitation of one nation by another will also be put an end to. In proportion as the antagonism
between classes within the nation vanishes, the hostility of one nation to another will come to an
end.
The charges against Communism made from a religious, a philosophical and, generally, from an
ideological standpoint, are not deserving of serious examination.
Does it require deep intuition to comprehend that man’s ideas, views, and conception, in one
word, man’s consciousness, changes with every change in the conditions of his material
existence, in his social relations and in his social life?
What else does the history of ideas prove, than that intellectual production changes its character
in proportion as material production is changed? The ruling ideas of each age have ever been the
ideas of its ruling class.
When people speak of the ideas that revolutionise society, they do but express that fact that
within the old society the elements of a new one have been created, and that the dissolution of the
old ideas keeps even pace with the dissolution of the old conditions of existence.
When the ancient world was in its last throes, the ancient religions were overcome by
Christianity. When Christian ideas succumbed in the 18th century to rationalist ideas, feudal 
26 Chapter II: Proletarians and Communists
society fought its death battle with the then revolutionary bourgeoisie. The ideas of religious
liberty and freedom of conscience merely gave expression to the sway of free competition within
the domain of knowledge.
“Undoubtedly,” it will be said, “religious, moral, philosophical, and juridical ideas have been
modified in the course of historical development. But religion, morality, philosophy, political
science, and law, constantly survived this change.”
“There are, besides, eternal truths, such as Freedom, Justice, etc., that are common to all states of
society. But Communism abolishes eternal truths, it abolishes all religion, and all morality,
instead of constituting them on a new basis; it therefore acts in contradiction to all past historical
experience.”
What does this accusation reduce itself to? The history of all past society has consisted in the
development of class antagonisms, antagonisms that assumed different forms at different epochs.
But whatever form they may have taken, one fact is common to all past ages, viz., the exploitation
of one part of society by the other. No wonder, then, that the social consciousness of past ages,
despite all the multiplicity and variety it displays, moves within certain common forms, or general
ideas, which cannot completely vanish except with the total disappearance of class antagonisms.
The Communist revolution is the most radical rupture with traditional property relations; no
wonder that its development involved the most radical rupture with traditional ideas.
But let us have done with the bourgeois objections to Communism.
We have seen above, that the first step in the revolution by the working class is to raise the
proletariat to the position of ruling class to win the battle of democracy.
The proletariat will use its political supremacy to wrest, by degree, all capital from the
bourgeoisie, to centralise all instruments of production in the hands of the State, i.e., of the
proletariat organised as the ruling class; and to increase the total productive forces as rapidly as
possible.
Of course, in the beginning, this cannot be effected except by means of despotic inroads on the
rights of property, and on the conditions of bourgeois production; by means of measures,
therefore, which appear economically insufficient and untenable, but which, in the course of the
movement, outstrip themselves, necessitate further inroads upon the old social order, and are
unavoidable as a means of entirely revolutionising the mode of production.
These measures will, of course, be different in different countries.
Nevertheless, in most advanced countries, the following will be pretty generally applicable.
1. Abolition of property in land and application of all rents of land to public
purposes.
2. A heavy progressive or graduated income tax.
3. Abolition of all rights of inheritance.
4. Confiscation of the property of all emigrants and rebels.
5. Centralisation of credit in the hands of the state, by means of a national bank
with State capital and an exclusive monopoly.
6. Centralisation of the means of communication and transport in the hands of the
State.
7. Extension of factories and instruments of production owned by the State; the
bringing into cultivation of waste-lands, and the improvement of the soil generally
in accordance with a common plan.
8. Equal liability of all to work. Establishment of industrial armies, especially for
agriculture.
9. Combination of agriculture with manufacturing industries; gradual abolition of
all the distinction between town and country by a more equable distribution of the 
27 Chapter II: Proletarians and Communists
populace over the country.
10. Free education for all children in public schools. Abolition of children’s
factory labour in its present form. Combination of education with industrial
production, &c, &c.
When, in the course of development, class distinctions have disappeared, and all production has
been concentrated in the hands of a vast association of the whole nation, the public power will
lose its political character. Political power, properly so called, is merely the organised power of
one class for oppressing another. If the proletariat during its contest with the bourgeoisie is
compelled, by the force of circumstances, to organise itself as a class, if, by means of a
revolution, it makes itself the ruling class, and, as such, sweeps away by force the old conditions
of production, then it will, along with these conditions, have swept away the conditions for the
existence of class antagonisms and of classes generally, and will thereby have abolished its own
supremacy as a class.
In place of the old bourgeois society, with its classes and class antagonisms, we shall have an
association, in which the free development of each is the condition for the free development of
all. 
III. Socialist and Communist Literature
1. Reactionary Socialism
A. Feudal Socialism
Owing to their historical position, it became the vocation of the aristocracies of France and
England to write pamphlets against modern bourgeois society. In the French Revolution of July
1830, and in the English reform agitation4
, these aristocracies again succumbed to the hateful
upstart. Thenceforth, a serious political struggle was altogether out of the question. A literary
battle alone remained possible. But even in the domain of literature the old cries of the restoration
period had become impossible.*
In order to arouse sympathy, the aristocracy was obliged to lose sight, apparently, of its own
interests, and to formulate their indictment against the bourgeoisie in the interest of the exploited
working class alone. Thus, the aristocracy took their revenge by singing lampoons on their new
masters and whispering in his ears sinister prophesies of coming catastrophe.
In this way arose feudal Socialism: half lamentation, half lampoon; half an echo of the past, half
menace of the future; at times, by its bitter, witty and incisive criticism, striking the bourgeoisie
to the very heart’s core; but always ludicrous in its effect, through total incapacity to comprehend
the march of modern history.
The aristocracy, in order to rally the people to them, waved the proletarian alms-bag in front for a
banner. But the people, so often as it joined them, saw on their hindquarters the old feudal coats
of arms, and deserted with loud and irreverent laughter.
One section of the French Legitimists and “Young England” exhibited this spectacle.
In pointing out that their mode of exploitation was different to that of the bourgeoisie, the
feudalists forget that they exploited under circumstances and conditions that were quite different
and that are now antiquated. In showing that, under their rule, the modern proletariat never
existed, they forget that the modern bourgeoisie is the necessary offspring of their own form of
society.
For the rest, so little do they conceal the reactionary character of their criticism that their chief
accusation against the bourgeois amounts to this, that under the bourgeois régime a class is being
developed which is destined to cut up root and branch the old order of society.
What they upbraid the bourgeoisie with is not so much that it creates a proletariat as that it creates
a revolutionary proletariat.
In political practice, therefore, they join in all coercive measures against the working class; and in
ordinary life, despite their high-falutin phrases, they stoop to pick up the golden apples dropped
from the tree of industry, and to barter truth, love, and honour, for traffic in wool, beetroot-sugar,
and potato spirits.†
As the parson has ever gone hand in hand with the landlord, so has Clerical Socialism with
Feudal Socialism.
 * Not the English Restoration (1660-1689), but the French Restoration (1814-1830). [Note by Engels to the English
edition of 1888.]
† This applies chiefly to Germany, where the landed aristocracy and squirearchy have large portions of their estates
cultivated for their own account by stewards, and are, moreover, extensive beetroot-sugar manufacturers and distillers
of potato spirits. The wealthier British aristocracy are, as yet, rather above that; but they, too, know how to make up for
declining rents by lending their names to floaters or more or less shady joint-stock companies. [Note by Engels to the
English edition of 1888.]
29 Chapter III: Socialist and Communist Literature
Nothing is easier than to give Christian asceticism a Socialist tinge. Has not Christianity
declaimed against private property, against marriage, against the State? Has it not preached in the
place of these, charity and poverty, celibacy and mortification of the flesh, monastic life and
Mother Church? Christian Socialism is but the holy water with which the priest consecrates the
heart-burnings of the aristocrat.
B. Petty-Bourgeois Socialism
The feudal aristocracy was not the only class that was ruined by the bourgeoisie, not the only
class whose conditions of existence pined and perished in the atmosphere of modern bourgeois
society. The medieval burgesses and the small peasant proprietors were the precursors of the
modern bourgeoisie. In those countries which are but little developed, industrially and
commercially, these two classes still vegetate side by side with the rising bourgeoisie.
In countries where modern civilisation has become fully developed, a new class of petty
bourgeois has been formed, fluctuating between proletariat and bourgeoisie, and ever renewing
itself as a supplementary part of bourgeois society. The individual members of this class,
however, are being constantly hurled down into the proletariat by the action of competition, and,
as modern industry develops, they even see the moment approaching when they will completely
disappear as an independent section of modern society, to be replaced in manufactures,
agriculture and commerce, by overlookers, bailiffs and shopmen.
In countries like France, where the peasants constitute far more than half of the population, it was
natural that writers who sided with the proletariat against the bourgeoisie should use, in their
criticism of the bourgeois régime, the standard of the peasant and petty bourgeois, and from the
standpoint of these intermediate classes, should take up the cudgels for the working class. Thus
arose petty-bourgeois Socialism. Sismondi was the head of this school, not only in France but
also in England.
This school of Socialism dissected with great acuteness the contradictions in the conditions of
modern production. It laid bare the hypocritical apologies of economists. It proved,
incontrovertibly, the disastrous effects of machinery and division of labour; the concentration of
capital and land in a few hands; overproduction and crises; it pointed out the inevitable ruin of the
petty bourgeois and peasant, the misery of the proletariat, the anarchy in production, the crying
inequalities in the distribution of wealth, the industrial war of extermination between nations, the
dissolution of old moral bonds, of the old family relations, of the old nationalities.
In its positive aims, however, this form of Socialism aspires either to restoring the old means of
production and of exchange, and with them the old property relations, and the old society, or to
cramping the modern means of production and of exchange within the framework of the old
property relations that have been, and were bound to be, exploded by those means. In either case,
it is both reactionary and Utopian.
Its last words are: corporate guilds for manufacture; patriarchal relations in agriculture.
Ultimately, when stubborn historical facts had dispersed all intoxicating effects of self-deception,
this form of Socialism ended in a miserable fit of the blues.
C. German or “True” Socialism
The Socialist and Communist literature of France, a literature that originated under the pressure
of a bourgeoisie in power, and that was the expressions of the struggle against this power, was
introduced into Germany at a time when the bourgeoisie, in that country, had just begun its
contest with feudal absolutism.
German philosophers, would-be philosophers, and beaux esprits (men of letters), eagerly seized
on this literature, only forgetting, that when these writings immigrated from France into
Germany, French social conditions had not immigrated along with them. In contact with German 
30 Chapter III: Socialist and Communist Literature
social conditions, this French literature lost all its immediate practical significance and assumed a
purely literary aspect. Thus, to the German philosophers of the Eighteenth Century, the demands
of the first French Revolution were nothing more than the demands of “Practical Reason” in
general, and the utterance of the will of the revolutionary French bourgeoisie signified, in their
eyes, the laws of pure Will, of Will as it was bound to be, of true human Will generally.
The work of the German literati consisted solely in bringing the new French ideas into harmony
with their ancient philosophical conscience, or rather, in annexing the French ideas without
deserting their own philosophic point of view.
This annexation took place in the same way in which a foreign language is appropriated, namely,
by translation.
It is well known how the monks wrote silly lives of Catholic Saints over the manuscripts on
which the classical works of ancient heathendom had been written. The German literati reversed
this process with the profane French literature. They wrote their philosophical nonsense beneath
the French original. For instance, beneath the French criticism of the economic functions of
money, they wrote “Alienation of Humanity”, and beneath the French criticism of the bourgeois
state they wrote “Dethronement of the Category of the General”, and so forth.
The introduction of these philosophical phrases at the back of the French historical criticisms,
they dubbed “Philosophy of Action”, “True Socialism”, “German Science of Socialism”,
“Philosophical Foundation of Socialism”, and so on.
The French Socialist and Communist literature was thus completely emasculated. And, since it
ceased in the hands of the German to express the struggle of one class with the other, he felt
conscious of having overcome “French one-sidedness” and of representing, not true requirements,
but the requirements of Truth; not the interests of the proletariat, but the interests of Human
Nature, of Man in general, who belongs to no class, has no reality, who exists only in the misty
realm of philosophical fantasy.
This German socialism, which took its schoolboy task so seriously and solemnly, and extolled its
poor stock-in-trade in such a mountebank fashion, meanwhile gradually lost its pedantic
innocence.
The fight of the Germans, and especially of the Prussian bourgeoisie, against feudal aristocracy
and absolute monarchy, in other words, the liberal movement, became more earnest.
By this, the long-wished for opportunity was offered to “True” Socialism of confronting the
political movement with the Socialist demands, of hurling the traditional anathemas against
liberalism, against representative government, against bourgeois competition, bourgeois freedom
of the press, bourgeois legislation, bourgeois liberty and equality, and of preaching to the masses
that they had nothing to gain, and everything to lose, by this bourgeois movement. German
Socialism forgot, in the nick of time, that the French criticism, whose silly echo it was,
presupposed the existence of modern bourgeois society, with its corresponding economic
conditions of existence, and the political constitution adapted thereto, the very things those
attainment was the object of the pending struggle in Germany.
To the absolute governments, with their following of parsons, professors, country squires, and
officials, it served as a welcome scarecrow against the threatening bourgeoisie.
It was a sweet finish, after the bitter pills of flogging and bullets, with which these same
governments, just at that time, dosed the German working-class risings.
While this “True” Socialism thus served the government as a weapon for fighting the German
bourgeoisie, it, at the same time, directly represented a reactionary interest, the interest of German
Philistines. In Germany, the petty-bourgeois class, a relic of the sixteenth century, and since then
constantly cropping up again under the various forms, is the real social basis of the existing state
of things. 
31 Chapter III: Socialist and Communist Literature
To preserve this class is to preserve the existing state of things in Germany. The industrial and
political supremacy of the bourgeoisie threatens it with certain destruction – on the one hand,
from the concentration of capital; on the other, from the rise of a revolutionary proletariat. “True”
Socialism appeared to kill these two birds with one stone. It spread like an epidemic.
The robe of speculative cobwebs, embroidered with flowers of rhetoric, steeped in the dew of
sickly sentiment, this transcendental robe in which the German Socialists wrapped their sorry
“eternal truths”, all skin and bone, served to wonderfully increase the sale of their goods amongst
such a public.
And on its part German Socialism recognised, more and more, its own calling as the bombastic
representative of the petty-bourgeois Philistine.
It proclaimed the German nation to be the model nation, and the German petty Philistine to be the
typical man. To every villainous meanness of this model man, it gave a hidden, higher, Socialistic
interpretation, the exact contrary of its real character. It went to the extreme length of directly
opposing the “brutally destructive” tendency of Communism, and of proclaiming its supreme and
impartial contempt of all class struggles. With very few exceptions, all the so-called Socialist and
Communist publications that now (1847) circulate in Germany belong to the domain of this foul
and enervating literature.*
2. Conservative or Bourgeois Socialism
A part of the bourgeoisie is desirous of redressing social grievances in order to secure the
continued existence of bourgeois society.
To this section belong economists, philanthropists, humanitarians, improvers of the condition of
the working class, organisers of charity, members of societies for the prevention of cruelty to
animals, temperance fanatics, hole-and-corner reformers of every imaginable kind. This form of
socialism has, moreover, been worked out into complete systems.
We may cite Proudhon’s Philosophie de la Misère as an example of this form.
The Socialistic bourgeois want all the advantages of modern social conditions without the
struggles and dangers necessarily resulting therefrom. They desire the existing state of society,
minus its revolutionary and disintegrating elements. They wish for a bourgeoisie without a
proletariat. The bourgeoisie naturally conceives the world in which it is supreme to be the best;
and bourgeois Socialism develops this comfortable conception into various more or less complete
systems. In requiring the proletariat to carry out such a system, and thereby to march straightway
into the social New Jerusalem, it but requires in reality, that the proletariat should remain within
the bounds of existing society, but should cast away all its hateful ideas concerning the
bourgeoisie.
A second, and more practical, but less systematic, form of this Socialism sought to depreciate
every revolutionary movement in the eyes of the working class by showing that no mere political
reform, but only a change in the material conditions of existence, in economical relations, could
be of any advantage to them. By changes in the material conditions of existence, this form of
Socialism, however, by no means understands abolition of the bourgeois relations of production,
an abolition that can be affected only by a revolution, but administrative reforms, based on the
continued existence of these relations; reforms, therefore, that in no respect affect the relations
between capital and labour, but, at the best, lessen the cost, and simplify the administrative work,
of bourgeois government.
 * The revolutionary storm of 1848 swept away this whole shabby tendency and cured its protagonists of the desire to
dabble in socialism. The chief representative and classical type of this tendency is Mr Karl Gruen. [Note by Engels to
the German edition of 1890.]
32 Chapter III: Socialist and Communist Literature
Bourgeois Socialism attains adequate expression when, and only when, it becomes a mere figure
of speech.
Free trade: for the benefit of the working class. Protective duties: for the benefit of the working
class. Prison Reform: for the benefit of the working class. This is the last word and the only
seriously meant word of bourgeois socialism.
It is summed up in the phrase: the bourgeois is a bourgeois – for the benefit of the working class.
3. Critical-Utopian Socialism and Communism
We do not here refer to that literature which, in every great modern revolution, has always given
voice to the demands of the proletariat, such as the writings of Babeuf and others.
The first direct attempts of the proletariat to attain its own ends, made in times of universal
excitement, when feudal society was being overthrown, necessarily failed, owing to the then
undeveloped state of the proletariat, as well as to the absence of the economic conditions for its
emancipation, conditions that had yet to be produced, and could be produced by the impending
bourgeois epoch alone. The revolutionary literature that accompanied these first movements of
the proletariat had necessarily a reactionary character. It inculcated universal asceticism and
social levelling in its crudest form.
The Socialist and Communist systems, properly so called, those of Saint-Simon, Fourier, Owen,
and others, spring into existence in the early undeveloped period, described above, of the struggle
between proletariat and bourgeoisie (see Section I. Bourgeois and Proletarians).
The founders of these systems see, indeed, the class antagonisms, as well as the action of the
decomposing elements in the prevailing form of society. But the proletariat, as yet in its infancy,
offers to them the spectacle of a class without any historical initiative or any independent political
movement.
Since the development of class antagonism keeps even pace with the development of industry, the
economic situation, as they find it, does not as yet offer to them the material conditions for the
emancipation of the proletariat. They therefore search after a new social science, after new social
laws, that are to create these conditions.
Historical action is to yield to their personal inventive action; historically created conditions of
emancipation to fantastic ones; and the gradual, spontaneous class organisation of the proletariat
to an organisation of society especially contrived by these inventors. Future history resolves
itself, in their eyes, into the propaganda and the practical carrying out of their social plans.
In the formation of their plans, they are conscious of caring chiefly for the interests of the
working class, as being the most suffering class. Only from the point of view of being the most
suffering class does the proletariat exist for them.
The undeveloped state of the class struggle, as well as their own surroundings, causes Socialists
of this kind to consider themselves far superior to all class antagonisms. They want to improve
the condition of every member of society, even that of the most favoured. Hence, they habitually
appeal to society at large, without the distinction of class; nay, by preference, to the ruling class.
For how can people, when once they understand their system, fail to see in it the best possible
plan of the best possible state of society?
Hence, they reject all political, and especially all revolutionary action; they wish to attain their
ends by peaceful means, necessarily doomed to failure, and by the force of example, to pave the
way for the new social Gospel.
Such fantastic pictures of future society, painted at a time when the proletariat is still in a very
undeveloped state and has but a fantastic conception of its own position, correspond with the first
instinctive yearnings of that class for a general reconstruction of society. 
33 Chapter III: Socialist and Communist Literature
But these Socialist and Communist publications contain also a critical element. They attack every
principle of existing society. Hence, they are full of the most valuable materials for the
enlightenment of the working class. The practical measures proposed in them – such as the
abolition of the distinction between town and country, of the family, of the carrying on of
industries for the account of private individuals, and of the wage system, the proclamation of
social harmony, the conversion of the function of the state into a mere superintendence of
production – all these proposals point solely to the disappearance of class antagonisms which
were, at that time, only just cropping up, and which, in these publications, are recognised in their
earliest indistinct and undefined forms only. These proposals, therefore, are of a purely Utopian
character.
The significance of Critical-Utopian Socialism and Communism bears an inverse relation to
historical development. In proportion as the modern class struggle develops and takes definite
shape, this fantastic standing apart from the contest, these fantastic attacks on it, lose all practical
value and all theoretical justification. Therefore, although the originators of these systems were,
in many respects, revolutionary, their disciples have, in every case, formed mere reactionary
sects. They hold fast by the original views of their masters, in opposition to the progressive
historical development of the proletariat. They, therefore, endeavour, and that consistently, to
deaden the class struggle and to reconcile the class antagonisms. They still dream of experimental
realisation of their social Utopias, of founding isolated “phalansteres”, of establishing “Home
Colonies”, or setting up a “Little Icaria”* – duodecimo editions of the New Jerusalem – and to
realise all these castles in the air, they are compelled to appeal to the feelings and purses of the
bourgeois. By degrees, they sink into the category of the reactionary [or] conservative Socialists
depicted above, differing from these only by more systematic pedantry, and by their fanatical and
superstitious belief in the miraculous effects of their social science.
They, therefore, violently oppose all political action on the part of the working class; such action,
according to them, can only result from blind unbelief in the new Gospel.
The Owenites in England, and the Fourierists in France, respectively, oppose the Chartists and the
Réformistes.
 * Phalanstéres were Socialist colonies on the plan of Charles Fourier; Icaria was the name given by Cabet to his Utopia
and, later on, to his American Communist colony. [Note by Engels to the English edition of 1888.]
“Home Colonies” were what Owen called his Communist model societies. Phalanstéres was the name of the public
palaces planned by Fourier. Icaria was the name given to the Utopian land of fancy, whose Communist institutions
Cabet portrayed. [Note by Engels to the German edition of 1890.]
IV. Position of the Communists in Relation to the
Various Existing Opposition Parties
Section II has made clear the relations of the Communists to the existing working-class parties,
such as the Chartists in England and the Agrarian Reformers in America.
The Communists fight for the attainment of the immediate aims, for the enforcement of the
momentary interests of the working class; but in the movement of the present, they also represent
and take care of the future of that movement. In France, the Communists ally with the SocialDemocrats* against the conservative and radical bourgeoisie, reserving, however, the right to take
up a critical position in regard to phases and illusions traditionally handed down from the great
Revolution.
In Switzerland, they support the Radicals, without losing sight of the fact that this party consists
of antagonistic elements, partly of Democratic Socialists, in the French sense, partly of radical
bourgeois.
In Poland, they support the party that insists on an agrarian revolution as the prime condition for
national emancipation, that party which fomented the insurrection of Cracow in 1846.
In Germany, they fight with the bourgeoisie whenever it acts in a revolutionary way, against the
absolute monarchy, the feudal squirearchy, and the petty bourgeoisie.
But they never cease, for a single instant, to instil into the working class the clearest possible
recognition of the hostile antagonism between bourgeoisie and proletariat, in order that the
German workers may straightway use, as so many weapons against the bourgeoisie, the social
and political conditions that the bourgeoisie must necessarily introduce along with its supremacy,
and in order that, after the fall of the reactionary classes in Germany, the fight against the
bourgeoisie itself may immediately begin.
The Communists turn their attention chiefly to Germany, because that country is on the eve of a
bourgeois revolution that is bound to be carried out under more advanced conditions of European
civilisation and with a much more developed proletariat than that of England was in the
seventeenth, and France in the eighteenth century, and because the bourgeois revolution in
Germany will be but the prelude to an immediately following proletarian revolution.
In short, the Communists everywhere support every revolutionary movement against the existing
social and political order of things.
In all these movements, they bring to the front, as the leading question in each, the property
question, no matter what its degree of development at the time.
Finally, they labour everywhere for the union and agreement of the democratic parties of all
countries.
The Communists disdain to conceal their views and aims. They openly declare that their ends can
be attained only by the forcible overthrow of all existing social conditions. Let the ruling classes
tremble at a Communistic revolution. The proletarians have nothing to lose but their chains. They
have a world to win.
Working Men of All Countries, Unite!5
 * The party then represented in Parliament by Ledru-Rollin, in literature by Louis Blanc, in the daily
press by the Réforme. The name of Social-Democracy signifies, with these its inventors, a section of
the Democratic or Republican Party more or less tinged with socialism. [Engels, English Edition
1888]
Letter from Engels to Marx, 24 November 1847*
Paris, 23-24 November 1847
Dear Marx,
Not until this evening was it decided that I should be coming. Saturday evening, then, in Ostend,
Hôtel de la Couronne, just opposite the railway station beside the harbour, and Sunday morning
across the water. If you take the train that leaves between 4 and 5, you’ll arrive at about the
same time as I do. ...
Tuesday evening
Verte [PTO]
Give a little thought to the “Confession of Faith.” I think we would do best to abandon the
catechetical form and call the thing “Communist Manifesto.” Since a certain amount of history
has to be narrated in it, the form hitherto adopted is quite unsuitable. I shall be bringing with me
the one from here, which I did [“Principles of Communism”]; it is in simple narrative form, but
wretchedly worded, in a tearing hurry. I start off by asking: What is communism? and then
straight on to the proletariat – the history of its origins, how it differs from earlier workers,
development of the antithesis between the proletariat and the bourgeoisie, crises, conclusions. In
between, all kinds of secondary matter and, finally, the communists’ party policy, in so far as it
should be made public. The one here has not yet been submitted in its entirety for endorsement
but, save for a few quite minor points, I think I can get it through in such a form that at least there
is nothing in it which conflicts with our views. ...
 * From MECW Volume 38, p. 146; Written: 24 November 1847; First published: in Der Briefwechsel zwischen F.
Engels und K. Marx, 1913.
Draft of a Communist Confession of Faith*
This document is the draft programme discussed at the First Congress of the Communist League in
London on June 2-9, 1847.
The Congress was a final stage in the reorganisation of the League of the Just – an organisation of
German workers and craftsmen, which was founded in Paris in 1836-37 and soon acquired an
international character, having communities in Germany, France, Switzerland, Britain and Sweden.
The activity of Marx and Engels directed towards the ideological and organisational unity of the
socialists and advanced workers prompted the leaders of the League (Karl Schapper, Joseph Moll,
Heinrich Bauer), who resided in London front November 1846, to ask for their help in reorganising
the League and drafting its new program me. When Marx and Engels were convinced that the leaders
of the League of the Just were ready to accept the principles of scientific communism as its
programme they accepted the offer to join the League made to them late in January 1847.
Engels’ active participation in the work of the Congress (Marx was unable to go to London) affected
the course and the results of its proceedings. The League was renamed the Communist League, the old
motto of the League of the Just “All men are brothers” was replaced by a new, Marxist one: “Working
Men of All Countries, Unite! “ The draft programme and the draft Rules of the League were approved
at the last sitting on June 9, 1847.
The full text of the “Draft of a Communist Confession of Faith” (Credo) became known only in 1968.
It was found by the Swiss scholar Bert Andréas together with the draft Rules and the circular of the
First Congress to the members of the League in the archives of Joachim Friedrich Martens, an active
member of the Communist League, which are kept in the State and University Library in Hamburg.
This discovery made it possible to ascertain a number of important points in the history of the
Communist League and the drafting of its programme documents. It had been previously assumed that
the First Congress did no more than adopt a decision to draw up a programme and that the draft itself
was made by the London Central Authority of the Communist League (Joseph Moll, Karl Schapper
and Heinrich Bauer) after the Congress between June and August 1847. The new documents show that
the draft was ready by June 9, 1847 and that its author was Engels (the manuscript found in Martens’
archives, with the exception of some inserted words, the concluding sentence and the signatures of the
president and the secretary of the Congress, was written in Engels’ hand).
The document testifies to Engels’ great influence on the discussion of the programme at the Congress
– the formulation of the answers to most of the questions is a Marxist one. Besides, while drafting the
programme, Engels had to take into account that the members of the League had not yet freed
themselves from the influence of utopian ideas and this was reflected in the formulation of the first six
questions and answers. The form of a “revolutionary catechism” was also commonly used in the
League of the Just and other organisations of workers and craftsmen at the time. It may he assumed
that Engels intended to give greater precision to some of the formulations of the programme document
in the course of further discussion and revision.
After the First Congress of the Communist League, the “Draft of a Communist Confession of Faith”
was sent, together with the draft Rules, to the communities for discussion, the results of which were to
be taken into account at the time of the final approval of the programme and the Rules at the Second
Congress. When working on another, improved draft programme, the Principles of Communism, in
late October 1847, Engels made direct use of the “Confession of Faith”, as can be seen from the
coincidences of the texts, and also from references in the Principles to the earlier document when
Engels had apparently decided to leave formulations of some of the answers as they were.
 * From MECW Volume 6, p. 92; written by Engels, June 9 1847; first published in Gründungsdokumente des Bundes
der Kommunisten, Hamburg, 1969, in English in Birth of the Communist Manifesto, International Publishers, 1971.
37 Draft of a Communist Confession of Faith
A Communist Confession of Faith
Question 1: Are you a Communist?
Answer: Yes.
Question 2: What is the aim of the Communists?
Answer: To organise society in such a way that every member of it can develop
and use all his capabilities and powers in complete freedom and without thereby
infringing the basic conditions of this society.
Question 3: How do you wish to achieve this aim?
Answer: By the elimination of private property and its replacement by community
of property.
Question 4: On what do you base your community of property?
Answer: Firstly, on the mass of productive forces and means of subsistence
resulting from the development of industry, agriculture, trade and colonisation,
and on the possibility inherent in machinery, chemical and other resources of their
infinite extension.
Secondly, on the fact that in the consciousness or feeling of every individual there
exist certain irrefutable basic principles which, being the result of the whole of
historical development, require no proof.
Question 5: What are such principles?
Answer: For example, every individual strives to be happy. The happiness of the
individual is inseparable from the happiness of all, etc.
Question 6: How do you wish to prepare the way for your community of property?
Answer: By enlightening and uniting the proletariat.
Question 7: What is the proletariat?
Answer: The proletariat is that class of society which lives exclusively by its
labour and not on the profit from any kind of capital; that class whose weal and
woe, whose life and death, therefore, depend on the alternation of times of good
and bad business;. in a word, on the fluctuations of competition.
Question 8: Then there have not always been proletarians?
Answer: No. There have always been poor and working classes; and those who
worked were almost always the poor. But there have not always been proletarians,
just as competition has not always been free.
Question 9: How did the proletariat arise?
Answer: The proletariat came into being as a result of the introduction of the
machines which have been invented since the middle of the last century and the
most important of which are: the steam-engine, the spinning machine and the
power loom. These machines, which were very expensive and could therefore
only be purchased by rich people, supplanted the workers of the time, because by
the use of machinery it was possible to produce commodities more quickly and
cheaply than could the workers with their imperfect spinning wheels and handlooms. The machines thus delivered industry entirely into the hands of the big
capitalists and rendered the workers’ scanty property which consisted mainly of
their tools, looms, etc., quite worthless, so that the capitalist was left with
everything, the worker with nothing. In this way the factory system was 
38 Draft of a Communist Confession of Faith
introduced. Once the capitalists saw how advantageous this was for them, they
sought to extend it to more and more branches of labour. They divided work more
and more between the workers so that workers who formerly had made a whole
article now produced only a part of it. Labour simplified in this way produced
goods more quickly and therefore more cheaply and only now was it found in
almost every branch of labour that here also machines could be used. As soon as
any branch of labour went over to factory production it ended up, just as in the
case of spinning and weaving. in the hands of the big capitalists, and the workers
were deprived of the last remnants of their independence. We have gradually
arrived at the position where almost all branches of labour are run on a factory
basis. This has increasingly brought about the ruin of the previously existing
middle class, especially of the small master craftsmen, completely transformed the
previous position of the workers, and two new classes which are gradually
swallowing up all other classes have come into being, namely:
I. The, class of the big capitalists, who in all advanced countries are in almost
exclusive possession of the means of subsistence and those means (machines,
factories, workshops, etc.) by which these means of subsistence are produced.
This is the bourgeois class, or the bourgeoisie.
II. The class of the completely propertyless, who are compelled to sell their labour
to the first class, the bourgeois, simply to obtain from them in return their means
of subsistence. Since the parties to this trading in labour are not equal, but the
bourgeois have the advantage, the propertyless must submit to the bad conditions
laid down by the bourgeois. This class, dependent on the bourgeois, is called the
class of the proletarians or the proletariat.
Question 10: In what way does the proletarian differ from the slave?
Answer: The slave is sold once and for all, the proletarian has to sell himself by
the day and by the hour. The slave is the property of one master and for that very
reason has a guaranteed subsistence, however wretched it may be. The proletarian
is, so to speak, the slave of the entire bourgeois class, not of one master, and
therefore has no guaranteed subsistence, since nobody buys his labour if he does
not need it. The slave is accounted a thing and not a member of civil society. The
proletarian is recognised as a person, as a member of civil society. The slave may,
therefore, have a better subsistence than the proletarian but the latter stands at a
higher stage of development. The slave frees himself by becoming a proletarian,
abolishing from the totality of property relationships only the relationship of
slavery. The proletarian can free himself only by abolishing property in general.
Question 11: In what way does the proletarian differ from the serf?
Answer: The serf has the use of a piece of land, that is, of an instrument of
production, in return for handing over a greater or lesser portion of the yield. The
proletarian works with instruments of production which belong to someone else
who, in return for his labour, hands over to him a portion, determined by
competition, of the products. In the case of the serf, the share of the labourer is
determined by his own labour, that is, by himself. In the case of the proletarian it
is determined by competition, therefore in the first place by the bourgeois. The
serf has guaranteed subsistence, the proletarian has not. The serf frees himself by
driving out his feudal lord and becoming a property owner himself, thus entering
into competition and joining for the time being the possessing class, the privileged
class. The proletarian frees himself by doing away with property, competition, and
all class differences.
39 Draft of a Communist Confession of Faith
Question 12: In what way does the proletarian differ from the handicraftsman?
Answer: As opposed to the proletarian, the so-called handicraftsman, who still
existed nearly everywhere during the last century and still exists here and there, is
at most a temporary proletarian. His aim is to acquire capital himself and so to
exploit other workers. He can often achieve this aim where the craft guilds still
exist or where freedom to follow a trade has not yet led to the organisation of
handwork on a factory basis and to intense competition. But as soon as the factory
system is introduced into handwork and competition is in full swing, this prospect
is eliminated and the handicraftsman becomes more and more a proletarian. The
handicraftsman therefore frees himself either by becoming a bourgeois or in
general passing over into the middle class, or, by becoming a proletarian as a
result of competition (as now happens in most cases) and joining the movement of
the proletariat – i. e., the more or less conscious communist movement.
Question 13: Then you do not believe that community of property has been possible at any time?
Answer: No. Communism has only arisen since machinery and other inventions
made it possible to hold out the prospect of an all-sided development, a happy
existence, for all members of society. Communism is the theory of a liberation
which was not possible for the slaves, the serfs, or the handicraftsmen, but only
for the proletarians and hence it belongs of necessity to the 19th century and was
not possible in any earlier period.
Question 14: Let m go back to the sixth question. As you wish to prepare for community of
property by the enlightening and uniting of the proletariat, then you reject revolution?
Answer: We are convinced not only of the uselessness but even of the
harmfulness of all conspiracies. We are also aware that revolutions are not made
deliberately and arbitrarily but that everywhere and at all times they are the
necessary consequence of circumstances which are not in any way whatever
dependent either on the will or on the leadership of individual parties or of whole
classes. But we also see that the development of the proletariat in almost all
countries of the world is forcibly repressed by the possessing classes and that thus
a revolution is being forcibly worked for by the opponents of communism. If, in
the end, the oppressed proletariat is thus driven into a revolution, then we will
defend the cause of the proletariat just as well by our deeds as now by our words.
Question 15: Do you intend to replace the existing social order by community of Property at one
stroke?
Answer: We have no such intention. The development of the masses cannot he
ordered by decree. It is determined by the development of the conditions in which
these masses live, and therefore proceeds gradually.
Question 16: How do you think the transition from the present situation to community of
Property is to be effected?
Answer: The first, fundamental condition for the introduction of community of
property is the political liberation of the proletariat through a democratic
constitution.
Question 17: What will be your first measure once you have established democracy?
Answer: Guaranteeing the subsistence of the proletariat.
Question 18: How will you do this?
40 Draft of a Communist Confession of Faith
Answer. I. By limiting private property in such a way that it gradually prepares
the way for its transformation into social property, e. g., by progressive taxation,
limitation of the right of inheritance in favour of the state, etc., etc.
II. By employing workers in national workshops and factories and on national
estates.
III. By educating all children at the expense of the state.
Question 19: How will you arrange this kind of education during the period of transition?
Answer: All children will be educated in state establishments from the time when
they can do without the first maternal care.
Question 20: Will not the introduction of community of property be accompanied by the
proclamation of the community of women?
Answer: By no means. We will only interfere in the personal relationship between
men and women or with the family in general to the extent that the maintenance of
the existing institution would disturb the new social order. Besides, we are well
aware that the family relationship has been modified in the course of history by
the property relationships and by periods of development, and that consequently
the ending of private property will also have a most important influence on it.
Question 21: Will nationalities continue to exist under communism?
Answer: The nationalities of the peoples who join together according to the
principle of community will be just as much compelled by this union to merge
with one another and thereby supersede themselves as the various differences
between estates and classes disappear through the superseding of their basis –
private property.
Question 22. Do Communists reject existing religions?
Answer: All religions which have existed hitherto were expressions of historical
stages of development of individual peoples or groups of peoples. But
communism is that stage of historical development which makes all existing
religions superfluous and supersedes them.
In the name and on the mandate of the Congress.
Secretary: Heide [Alias of Wilhelm Wolff in the League of the Just]
President: Karl Schill [Alias of Karl Schapper in the League of the Just]
London, June 9, 1847
The Principles of Communism*
In 1847 Engels wrote two draft programmes for the Communist League in the form of a catechism,
one in June and the other in October. The latter, which is known as Principles of Communism, was
first published in 1914. The earlier document “Draft of the Communist Confession of Faith”, was only
found in 1968. It was first published in 1969 in Hamburg, together with four other documents
pertaining to the first congress of the Communist League, in a booklet entitled Gründungs Dokumente
des Bundes der Kommunisten (Juni bis September 1847) [Founding Documents of the Communist
League].
At the June 1847 Congress of the League of the Just, which was also the founding conference of the
Communist League, it was decided to issue a draft “confession of faith” to be submitted for discussion
to the sections of the League. The document which has now come to light is almost certainly this
draft. Comparison of the two documents shows that Principles of Communism is a revised edition of
this earlier draft. In Principles of Communism, Engels left three questions unanswered, in two cases
with the notation “unchanged” (bleibt); this clearly refers to the answers provided in the earlier draft.
The new draft for the programme was worked out by Engels on the instructions of the leading body of
the Paris circle of the Communist League. The instructions were decided on after Engels’ sharp
criticism at the committee meeting, on October 22, 1847, of the draft programme drawn up by the
“true socialist“ Moses Hess, which was then rejected.
Still considering Principles of Communism as a preliminary draft, Engels expressed the view, in a
letter to Marx dated November 23-24 1847, that it would be best to drop the old catechistic form and
draw up a programme in the form of a manifesto.
At the second congress of the Communist League (November 29-December 8, 1847) Marx and Engels
defended the fundamental scientific principles of communism and were trusted with drafting a
programme in the form of a manifesto of the Communist Party. In writing the manifesto the founders
of Marxism made use of the propositions enunciated in Principles of Communism.
Engels uses the term Manufaktur, and its derivatives, which have been translated “manufacture”,
“manufacturing”, etc., Engels used this word literally, to indicate production by hand, not factory
production for which Engels uses “big industry”. Manufaktur differs from handicraft (guild production
in mediaeval towns), in that the latter was carried out by independent artisans. Manufacktur is carried
out by homeworkers working for merchant capitalists, or by groups of craftspeople working together
in large workshops owned by capitalists. It is therefore a transitional mode of production, between
guild (handicraft) and modern (capitalist) forms of production.
 * Written: October-November 1847; Source: Selected Works, Volume One, p. 81-97, Progress Publishers, Moscow,
1969; first published: 1914, by Eduard Bernstein in the German Social Democratic Party’s Vorwärts!; translated: Paul
Sweezy; Transcribed: Zodiac, MEA 1993; marxists.org 1999; proofed and corrected by Andy Blunden, February 2005.
Footnotes are from the Chinese Edition of Marx/Engels Selected Works Peking, Foreign Languages Press, 1977, with
editorial additions by marxists.org.
42 Draft of a Communist Confession of Faith
The Principles of Communism
– 1 –
What is Communism?
Communism is the doctrine of the conditions of the liberation of the proletariat.
– 2 –
What is the proletariat?
The proletariat is that class in society which lives entirely from the sale of its labor and does not
draw profit from any kind of capital; whose weal and woe, whose life and death, whose sole
existence depends on the demand for labor – hence, on the changing state of business, on the
vagaries of unbridled competition. The proletariat, or the class of proletarians, is, in a word, the
working class of the 19th century.6
– 3 –
Proletarians, then, have not always existed?
No. There have always been poor and working classes; and the working class have mostly been
poor. But there have not always been workers and poor people living under conditions as they are
today; in other words, there have not always been proletarians, any more than there has always
been free unbridled competitions.
– 4 –
How did the proletariat originate?
The Proletariat originated in the industrial revolution, which took place in England in the last half
of the last (18th) century, and which has since then been repeated in all the civilized countries of
the world.
This industrial revolution was precipitated by the discovery of the steam engine, various spinning
machines, the mechanical loom, and a whole series of other mechanical devices. These machines,
which were very expensive and hence could be bought only by big capitalists, altered the whole
mode of production and displaced the former workers, because the machines turned out cheaper
and better commodities than the workers could produce with their inefficient spinning wheels and
handlooms. The machines delivered industry wholly into the hands of the big capitalists and
rendered entirely worthless the meagre property of the workers (tools, looms, etc.). The result was
that the capitalists soon had everything in their hands and nothing remained to the workers. This
marked the introduction of the factory system into the textile industry.
Once the impulse to the introduction of machinery and the factory system had been given, this
system spread quickly to all other branches of industry, especially cloth- and book-printing,
pottery, and the metal industries.
Labor was more and more divided among the individual workers so that the worker who
previously had done a complete piece of work now did only a part of that piece. This division of
labor made it possible to produce things faster and cheaper. It reduced the activity of the
individual worker to simple, endlessly repeated mechanical motions which could be performed
not only as well but much better by a machine. In this way, all these industries fell, one after
another, under the dominance of steam, machinery, and the factory system, just as spinning and
weaving had already done.
But at the same time, they also fell into the hands of big capitalists, and their workers were
deprived of whatever independence remained to them. Gradually, not only genuine manufacture
but also handicrafts came within the province of the factory system as big capitalists increasingly 
43 Draft of a Communist Confession of Faith
displaced the small master craftsmen by setting up huge workshops, which saved many expenses
and permitted an elaborate division of labor.
This is how it has come about that in civilized countries at the present time nearly all kinds of
labor are performed in factories – and, in nearly all branches of work, handicrafts and
manufacture have been superseded. This process has, to an ever greater degree, ruined the old
middle class, especially the small handicraftsmen; it has entirely transformed the condition of the
workers; and two new classes have been created which are gradually swallowing up all the others.
These are:
(i) The class of big capitalists, who, in all civilized countries, are already in almost
exclusive possession of all the means of subsistence and of the instruments
(machines, factories) and materials necessary for the production of the means of
subsistence. This is the bourgeois class, or the bourgeoisie.
(ii) The class of the wholly propertyless, who are obliged to sell their labor to the
bourgeoisie in order to get, in exchange, the means of subsistence for their
support. This is called the class of proletarians, or the proletariat.
– 5 –
Under what conditions does this sale of the
labor of the proletarians to the bourgeoisie take place?
Labor is a commodity, like any other, and its price is therefore determined by exactly the same
laws that apply to other commodities. In a regime of big industry or of free competition – as we
shall see, the two come to the same thing – the price of a commodity is, on the average, always
equal to its cost of production. Hence, the price of labor is also equal to the cost of production of
labor.
But, the costs of production of labor consist of precisely the quantity of means of subsistence
necessary to enable the worker to continue working, and to prevent the working class from dying
out. The worker will therefore get no more for his labor than is necessary for this purpose; the
price of labor, or the wage, will, in other words, be the lowest, the minimum, required for the
maintenance of life.
However, since business is sometimes better and sometimes worse, it follows that the worker
sometimes gets more and sometimes gets less for his commodities. But, again, just as the
industrialist, on the average of good times and bad, gets no more and no less for his commodities
than what they cost, similarly on the average the worker gets no more and no less than his
minimum.
This economic law of wages operates the more strictly the greater the degree to which big
industry has taken possession of all branches of production.
– 6 –
What working classes were there before the industrial
revolution?
The working classes have always, according to the different stages of development of society,
lived in different circumstances and had different relations to the owning and ruling classes.
In antiquity, the workers were the slaves of the owners, just as they still are in many backward
countries and even in the southern part of the United States.
In the Middle Ages, they were the serfs of the land-owning nobility, as they still are in Hungary,
Poland, and Russia. In the Middle Ages, and indeed right up to the industrial revolution, there
were also journeymen in the cities who worked in the service of petty bourgeois masters. 
44 Draft of a Communist Confession of Faith
Gradually, as manufacture developed, these journeymen became manufacturing workers who
were even then employed by larger capitalists.
– 7 –
In what way do proletarians differ from slaves?
The slave is sold once and for all; the proletarian must sell himself daily and hourly.
The individual slave, property of one master, is assured an existence, however miserable it may
be, because of the master’s interest. The individual proletarian, property as it were of the entire
bourgeois class which buys his labor only when someone has need of it, has no secure existence.
This existence is assured only to the class as a whole.
The slave is outside competition; the proletarian is in it and experiences all its vagaries.
The slave counts as a thing, not as a member of society. Thus, the slave can have a better
existence than the proletarian, while the proletarian belongs to a higher stage of social
development and, himself, stands on a higher social level than the slave.
The slave frees himself when, of all the relations of private property, he abolishes only the
relation of slavery and thereby becomes a proletarian; the proletarian can free himself only by
abolishing private property in general.
– 8 –
In what way do proletarians differ from serfs?
The serf possesses and uses an instrument of production, a piece of land, in exchange for which
he gives up a part of his product or part of the services of his labor.
The proletarian works with the instruments of production of another, for the account of this other,
in exchange for a part of the product.
The serf gives up, the proletarian receives. The serf has an assured existence, the proletarian has
not. The serf is outside competition, the proletarian is in it.
The serf liberates himself in one of three ways: either he runs away to the city and there becomes
a handicraftsman; or, instead of products and services, he gives money to his lord and thereby
becomes a free tenant; or he overthrows his feudal lord and himself becomes a property owner. In
short, by one route or another, he gets into the owning class and enters into competition. The
proletarian liberates himself by abolishing competition, private property, and all class differences.
– 9 –
In what way do proletarians differ from handicraftsmen?
In contrast to the proletarian, the so-called handicraftsman, as he still existed almost everywhere
in the past (eighteenth) century and still exists here and there at present, is a proletarian at most
temporarily. His goal is to acquire capital himself wherewith to exploit other workers. He can
often achieve this goal where guilds still exist or where freedom from guild restrictions has not
yet led to the introduction of factory-style methods into the crafts nor yet to fierce competition
But as soon as the factory system has been introduced into the crafts and competition flourishes
fully, this perspective dwindles away and the handicraftsman becomes more and more a
proletarian. The handicraftsman therefore frees himself by becoming either bourgeois or entering
the middle class in general, or becoming a proletarian because of competition (as is now more
often the case). In which case he can free himself by joining the proletarian movement, i.e., the
more or less communist movement.7
45 Draft of a Communist Confession of Faith
– 10 –
In what way do proletarians differ from manufacturing
workers?
The manufacturing worker of the 16th to the 18th centuries still had, with but few exception, an
instrument of production in his own possession – his loom, the family spinning wheel, a little plot
of land which he cultivated in his spare time. The proletarian has none of these things.
The manufacturing worker almost always lives in the countryside and in a more or less
patriarchal relation to his landlord or employer; the proletarian lives, for the most part, in the city
and his relation to his employer is purely a cash relation.
The manufacturing worker is torn out of his patriarchal relation by big industry, loses whatever
property he still has, and in this way becomes a proletarian.
– 11 –
What were the immediate consequences of the industrial
revolution and of the division of society into bourgeoisie
and proletariat?
First, the lower and lower prices of industrial products brought about by machine labor totally
destroyed, in all countries of the world, the old system of manufacture or industry based upon
hand labor.
In this way, all semi-barbarian countries, which had hitherto been more or less strangers to
historical development, and whose industry had been based on manufacture, were violently
forced out of their isolation. They bought the cheaper commodities of the English and allowed
their own manufacturing workers to be ruined. Countries which had known no progress for
thousands of years – for example, India – were thoroughly revolutionized, and even China is now
on the way to a revolution.
We have come to the point where a new machine invented in England deprives millions of
Chinese workers of their livelihood within a year’s time.
In this way, big industry has brought all the people of the Earth into contact with each other, has
merged all local markets into one world market, has spread civilization and progress everywhere
and has thus ensured that whatever happens in civilized countries will have repercussions in all
other countries.
It follows that if the workers in England or France now liberate themselves, this must set off
revolution in all other countries – revolutions which, sooner or later, must accomplish the
liberation of their respective working class.
Second, wherever big industries displaced manufacture, the bourgeoisie developed in wealth and
power to the utmost and made itself the first class of the country. The result was that wherever
this happened, the bourgeoisie took political power into its own hands and displaced the hitherto
ruling classes, the aristocracy, the guildmasters, and their representative, the absolute monarchy.
The bourgeoisie annihilated the power of the aristocracy, the nobility, by abolishing the
entailment of estates – in other words, by making landed property subject to purchase and sale,
and by doing away with the special privileges of the nobility. It destroyed the power of the
guildmasters by abolishing guilds and handicraft privileges. In their place, it put competition –
that is, a state of society in which everyone has the right to enter into any branch of industry, the
only obstacle being a lack of the necessary capital.
The introduction of free competition is thus public declaration that from now on the members of
society are unequal only to the extent that their capitals are unequal, that capital is the decisive
power, and that therefore the capitalists, the bourgeoisie, have become the first class in society. 
46 Draft of a Communist Confession of Faith
Free competition is necessary for the establishment of big industry, because it is the only
condition of society in which big industry can make its way.
Having destroyed the social power of the nobility and the guildmasters, the bourgeois also
destroyed their political power. Having raised itself to the actual position of first class in society,
it proclaims itself to be also the dominant political class. This it does through the introduction of
the representative system which rests on bourgeois equality before the law and the recognition of
free competition, and in European countries takes the form of constitutional monarchy. In these
constitutional monarchies, only those who possess a certain capital are voters – that is to say, only
members of the bourgeoisie. These bourgeois voters choose the deputies, and these bourgeois
deputies, by using their right to refuse to vote taxes, choose a bourgeois government.
Third, everywhere the proletariat develops in step with the bourgeoisie. In proportion, as the
bourgeoisie grows in wealth, the proletariat grows in numbers. For, since the proletarians can be
employed only by capital, and since capital extends only through employing labor, it follows that
the growth of the proletariat proceeds at precisely the same pace as the growth of capital.
Simultaneously, this process draws members of the bourgeoisie and proletarians together into the
great cities where industry can be carried on most profitably, and by thus throwing great masses
in one spot it gives to the proletarians a consciousness of their own strength.
Moreover, the further this process advances, the more new labor-saving machines are invented,
the greater is the pressure exercised by big industry on wages, which, as we have seen, sink to
their minimum and therewith render the condition of the proletariat increasingly unbearable. The
growing dissatisfaction of the proletariat thus joins with its rising power to prepare a proletarian
social revolution.
– 12 –
What were the further consequences of the industrial
revolution?
Big industry created in the steam engine, and other machines, the means of endlessly expanding
industrial production, speeding it up, and cutting its costs. With production thus facilitated, the
free competition, which is necessarily bound up with big industry, assumed the most extreme
forms; a multitude of capitalists invaded industry, and, in a short while, more was produced than
was needed.
As a consequence, finished commodities could not be sold, and a so-called commercial crisis
broke out. Factories had to be closed, their owners went bankrupt, and the workers were without
bread. Deepest misery reigned everywhere.
After a time, the superfluous products were sold, the factories began to operate again, wages rose,
and gradually business got better than ever.
But it was not long before too many commodities were again produced and a new crisis broke
out, only to follow the same course as its predecessor.
Ever since the beginning of this (19th) century, the condition of industry has constantly fluctuated
between periods of prosperity and periods of crisis; nearly every five to seven years, a fresh crisis
has intervened, always with the greatest hardship for workers, and always accompanied by
general revolutionary stirrings and the direct peril to the whole existing order of things.
– 13 –
What follows from these periodic commercial crises?
First:
That, though big industry in its earliest stage created free competition, it has now
outgrown free competition; 
47 Draft of a Communist Confession of Faith
that, for big industry, competition and generally the individualistic organization of
production have become a fetter which it must and will shatter;
that, so long as big industry remains on its present footing, it can be maintained
only at the cost of general chaos every seven years, each time threatening the
whole of civilization and not only plunging the proletarians into misery but also
ruining large sections of the bourgeoisie;
hence, either that big industry must itself be given up, which is an absolute
impossibility, or that it makes unavoidably necessary an entirely new organization
of society in which production is no longer directed by mutually competing
individual industrialists but rather by the whole society operating according to a
definite plan and taking account of the needs of all.
Second: That big industry, and the limitless expansion of production which it makes possible,
bring within the range of feasibility a social order in which so much is produced that every
member of society will be in a position to exercise and develop all his powers and faculties in
complete freedom.
It thus appears that the very qualities of big industry which, in our present-day society, produce
misery and crises are those which, in a different form of society, will abolish this misery and
these catastrophic depressions.
We see with the greatest clarity:
(i) That all these evils are from now on to be ascribed solely to a social order
which no longer corresponds to the requirements of the real situation; and
(ii) That it is possible, through a new social order, to do away with these evils
altogether.
– 14 –
What will this new social order have to be like?
Above all, it will have to take the control of industry and of all branches of production out of the
hands of mutually competing individuals, and instead institute a system in which all these
branches of production are operated by society as a whole – that is, for the common account,
according to a common plan, and with the participation of all members of society.
It will, in other words, abolish competition and replace it with association.
Moreover, since the management of industry by individuals necessarily implies private property,
and since competition is in reality merely the manner and form in which the control of industry
by private property owners expresses itself, it follows that private property cannot be separated
from competition and the individual management of industry. Private property must, therefore, be
abolished and in its place must come the common utilization of all instruments of production and
the distribution of all products according to common agreement – in a word, what is called the
communal ownership of goods.
In fact, the abolition of private property is, doubtless, the shortest and most significant way to
characterize the revolution in the whole social order which has been made necessary by the
development of industry – and for this reason it is rightly advanced by communists as their main
demand. 
48 Draft of a Communist Confession of Faith
– 15 –
Was not the abolition of private property possible at an
earlier time?
No. Every change in the social order, every revolution in property relations, is the necessary
consequence of the creation of new forces of production which no longer fit into the old property
relations.
Private property has not always existed.
When, towards the end of the Middle Ages, there arose a new mode of production which could
not be carried on under the then existing feudal and guild forms of property, this manufacture,
which had outgrown the old property relations, created a new property form, private property.
And for manufacture and the earliest stage of development of big industry, private property was
the only possible property form; the social order based on it was the only possible social order.
So long as it is not possible to produce so much that there is enough for all, with more left over
for expanding the social capital and extending the forces of production – so long as this is not
possible, there must always be a ruling class directing the use of society’s productive forces, and
a poor, oppressed class. How these classes are constituted depends on the stage of development.
The agrarian Middle Ages give us the baron and the serf; the cities of the later Middle Ages show
us the guildmaster and the journeyman and the day laborer; the 17th century has its
manufacturing workers; the 19th has big factory owners and proletarians.
It is clear that, up to now, the forces of production have never been developed to the point where
enough could be developed for all, and that private property has become a fetter and a barrier in
relation to the further development of the forces of production.
Now, however, the development of big industry has ushered in a new period. Capital and the
forces of production have been expanded to an unprecedented extent, and the means are at hand
to multiply them without limit in the near future. Moreover, the forces of production have been
concentrated in the hands of a few bourgeois, while the great mass of the people are more and
more falling into the proletariat, their situation becoming more wretched and intolerable in
proportion to the increase of wealth of the bourgeoisie. And finally, these mighty and easily
extended forces of production have so far outgrown private property and the bourgeoisie, that
they threaten at any moment to unleash the most violent disturbances of the social order. Now,
under these conditions, the abolition of private property has become not only possible but
absolutely necessary.
– 16 –
Will the peaceful abolition of private property be possible?
It would be desirable if this could happen, and the communists would certainly be the last to
oppose it. Communists know only too well that all conspiracies are not only useless, but even
harmful. They know all too well that revolutions are not made intentionally and arbitrarily, but
that, everywhere and always, they have been the necessary consequence of conditions which were
wholly independent of the will and direction of individual parties and entire classes.
But they also see that the development of the proletariat in nearly all civilized countries has been
violently suppressed, and that in this way the opponents of communism have been working
toward a revolution with all their strength. If the oppressed proletariat is finally driven to
revolution, then we communists will defend the interests of the proletarians with deeds as we now
defend them with words. 
49 Draft of a Communist Confession of Faith
– 17 –
Will it be possible for private property to be abolished at
one stroke?
No, no more than existing forces of production can at one stroke be multiplied to the extent
necessary for the creation of a communal society.
In all probability, the proletarian revolution will transform existing society gradually and will be
able to abolish private property only when the means of production are available in sufficient
quantity.
– 18 –
What will be the course of this revolution?
Above all, it will establish a democratic constitution, and through this, the direct or indirect
dominance of the proletariat. Direct in England, where the proletarians are already a majority of
the people. Indirect in France and Germany, where the majority of the people consists not only of
proletarians, but also of small peasants and petty bourgeois who are in the process of falling into
the proletariat, who are more and more dependent in all their political interests on the proletariat,
and who must, therefore, soon adapt to the demands of the proletariat. Perhaps this will cost a
second struggle, but the outcome can only be the victory of the proletariat.
Democracy would be wholly valueless to the proletariat if it were not immediately used as a
means for putting through measures directed against private property and ensuring the livelihood
of the proletariat. The main measures, emerging as the necessary result of existing relations, are
the following:
(i) Limitation of private property through progressive taxation, heavy inheritance
taxes, abolition of inheritance through collateral lines (brothers, nephews, etc.)
forced loans, etc.
(ii) Gradual expropriation of landowners, industrialists, railroad magnates and
shipowners, partly through competition by state industry, partly directly through
compensation in the form of bonds.
(iii) Confiscation of the possessions of all emigrants and rebels against the
majority of the people.
(iv) Organization of labor or employment of proletarians on publicly owned land,
in factories and workshops, with competition among the workers being abolished
and with the factory owners, in so far as they still exist, being obliged to pay the
same high wages as those paid by the state.
(v) An equal obligation on all members of society to work until such time as
private property has been completely abolished. Formation of industrial armies,
especially for agriculture.
(vi) Centralization of money and credit in the hands of the state through a national
bank with state capital, and the suppression of all private banks and bankers.
(vii) Increase in the number of national factories, workshops, railroads, ships;
bringing new lands into cultivation and improvement of land already under
cultivation – all in proportion to the growth of the capital and labor force at the
disposal of the nation.
(viii) Education of all children, from the moment they can leave their mother’s
care, in national establishments at national cost. Education and production
together. 
50 Draft of a Communist Confession of Faith
(ix) Construction, on public lands, of great palaces as communal dwellings for
associated groups of citizens engaged in both industry and agriculture and
combining in their way of life the advantages of urban and rural conditions while
avoiding the one-sidedness and drawbacks of each.
(x) Destruction of all unhealthy and jerry-built dwellings in urban districts.
(xi) Equal inheritance rights for children born in and out of wedlock.
(xii) Concentration of all means of transportation in the hands of the nation.
It is impossible, of course, to carry out all these measures at once. But one will always bring
others in its wake. Once the first radical attack on private property has been launched, the
proletariat will find itself forced to go ever further, to concentrate increasingly in the hands of the
state all capital, all agriculture, all transport, all trade. All the foregoing measures are directed to
this end; and they will become practicable and feasible, capable of producing their centralizing
effects to precisely the degree that the proletariat, through its labor, multiplies the country’s
productive forces.
Finally, when all capital, all production, all exchange have been brought together in the hands of
the nation, private property will disappear of its own accord, money will become superfluous, and
production will so expand and man so change that society will be able to slough off whatever of
its old economic habits may remain.
– 19 –
Will it be possible for this revolution to take place in one
country alone?
No. By creating the world market, big industry has already brought all the peoples of the Earth,
and especially the civilized peoples, into such close relation with one another that none is
independent of what happens to the others.
Further, it has co-ordinated the social development of the civilized countries to such an extent
that, in all of them, bourgeoisie and proletariat have become the decisive classes, and the struggle
between them the great struggle of the day. It follows that the communist revolution will not
merely be a national phenomenon but must take place simultaneously in all civilized countries –
that is to say, at least in England, America, France, and Germany.
It will develop in each of the these countries more or less rapidly, according as one country or the
other has a more developed industry, greater wealth, a more significant mass of productive forces.
Hence, it will go slowest and will meet most obstacles in Germany, most rapidly and with the
fewest difficulties in England. It will have a powerful impact on the other countries of the world,
and will radically alter the course of development which they have followed up to now, while
greatly stepping up its pace.
It is a universal revolution and will, accordingly, have a universal range.
– 20 –
What will be the consequences of the
ultimate disappearance of private property?
Society will take all forces of production and means of commerce, as well as the exchange and
distribution of products, out of the hands of private capitalists and will manage them in
accordance with a plan based on the availability of resources and the needs of the whole society.
In this way, most important of all, the evil consequences which are now associated with the
conduct of big industry will be abolished.
There will be no more crises; the expanded production, which for the present order of society is
overproduction and hence a prevailing cause of misery, will then be insufficient and in need of 
51 Draft of a Communist Confession of Faith
being expanded much further. Instead of generating misery, overproduction will reach beyond the
elementary requirements of society to assure the satisfaction of the needs of all; it will create new
needs and, at the same time, the means of satisfying them. It will become the condition of, and the
stimulus to, new progress, which will no longer throw the whole social order into confusion, as
progress has always done in the past. Big industry, freed from the pressure of private property,
will undergo such an expansion that what we now see will seem as petty in comparison as
manufacture seems when put beside the big industry of our own day. This development of
industry will make available to society a sufficient mass of products to satisfy the needs of
everyone.
The same will be true of agriculture, which also suffers from the pressure of private property and
is held back by the division of privately owned land into small parcels. Here, existing
improvements and scientific procedures will be put into practice, with a resulting leap forward
which will assure to society all the products it needs.
In this way, such an abundance of goods will be able to satisfy the needs of all its members.
The division of society into different, mutually hostile classes will then become unnecessary.
Indeed, it will be not only unnecessary but intolerable in the new social order. The existence of
classes originated in the division of labor, and the division of labor, as it has been known up to
the present, will completely disappear. For mechanical and chemical processes are not enough to
bring industrial and agricultural production up to the level we have described; the capacities of
the men who make use of these processes must undergo a corresponding development.
Just as the peasants and manufacturing workers of the last century changed their whole way of
life and became quite different people when they were drawn into big industry, in the same way,
communal control over production by society as a whole, and the resulting new development, will
both require an entirely different kind of human material.
People will no longer be, as they are today, subordinated to a single branch of production, bound
to it, exploited by it; they will no longer develop one of their faculties at the expense of all others;
they will no longer know only one branch, or one branch of a single branch, of production as a
whole. Even industry as it is today is finding such people less and less useful.
Industry controlled by society as a whole, and operated according to a plan, presupposes wellrounded human beings, their faculties developed in balanced fashion, able to see the system of
production in its entirety.
The form of the division of labor which makes one a peasant, another a cobbler, a third a factory
worker, a fourth a stock-market operator, has already been undermined by machinery and will
completely disappear. Education will enable young people quickly to familiarize themselves with
the whole system of production and to pass from one branch of production to another in response
to the needs of society or their own inclinations. It will, therefore, free them from the one-sided
character which the present-day division of labor impresses upon every individual. Communist
society will, in this way, make it possible for its members to put their comprehensively developed
faculties to full use. But, when this happens, classes will necessarily disappear. It follows that
society organized on a communist basis is incompatible with the existence of classes on the one
hand, and that the very building of such a society provides the means of abolishing class
differences on the other.
A corollary of this is that the difference between city and country is destined to disappear. The
management of agriculture and industry by the same people rather than by two different classes
of people is, if only for purely material reasons, a necessary condition of communist association.
The dispersal of the agricultural population on the land, alongside the crowding of the industrial
population into the great cities, is a condition which corresponds to an undeveloped state of both
agriculture and industry and can already be felt as an obstacle to further development. 
52 Draft of a Communist Confession of Faith
The general co-operation of all members of society for the purpose of planned exploitation of the
forces of production, the expansion of production to the point where it will satisfy the needs of
all, the abolition of a situation in which the needs of some are satisfied at the expense of the needs
of others, the complete liquidation of classes and their conflicts, the rounded development of the
capacities of all members of society through the elimination of the present division of labor,
through industrial education, through engaging in varying activities, through the participation by
all in the enjoyments produced by all, through the combination of city and country – these are the
main consequences of the abolition of private property.
– 21 –
What will be the influence of communist society on the
family?
It will transform the relations between the sexes into a purely private matter which concerns only
the persons involved and into which society has no occasion to intervene. It can do this since it
does away with private property and educates children on a communal basis, and in this way
removes the two bases of traditional marriage – the dependence rooted in private property, of the
women on the man, and of the children on the parents.
And here is the answer to the outcry of the highly moral philistines against the “community of
women”. Community of women is a condition which belongs entirely to bourgeois society and
which today finds its complete expression in prostitution. But prostitution is based on private
property and falls with it. Thus, communist society, instead of introducing community of women,
in fact abolishes it.
– 22 –
What will be the attitude of communism to existing
nationalities?
The nationalities of the peoples associating themselves in accordance with the principle of
community will be compelled to mingle with each other as a result of this association and thereby
to dissolve themselves, just as the various estate and class distinctions must disappear through the
abolition of their basis, private property.8
– 23 –
What will be its attitude to existing religions?
All religions so far have been the expression of historical stages of development of individual
peoples or groups of peoples. But communism is the stage of historical development which
makes all existing religions superfluous and brings about their disappearance.
9
– 24 –
How do communists differ from socialists?
The so-called socialists are divided into three categories.
[ Reactionary Socialists: ]
The first category consists of adherents of a feudal and patriarchal society which has already been
destroyed, and is still daily being destroyed, by big industry and world trade and their creation,
bourgeois society. This category concludes, from the evils of existing society, that feudal and
patriarchal society must be restored because it was free of such evils. In one way or another, all
their proposals are directed to this end. 
53 Draft of a Communist Confession of Faith
This category of reactionary socialists, for all their seeming partisanship and their scalding tears
for the misery of the proletariat, is nevertheless energetically opposed by the communists for the
following reasons:
(i) It strives for something which is entirely impossible.
(ii) It seeks to establish the rule of the aristocracy, the guildmasters, the small
producers, and their retinue of absolute or feudal monarchs, officials, soldiers, and
priests – a society which was, to be sure, free of the evils of present-day society
but which brought it at least as many evils without even offering to the oppressed
workers the prospect of liberation through a communist revolution.
(iii) As soon as the proletariat becomes revolutionary and communist, these
reactionary socialists show their true colors by immediately making common
cause with the bourgeoisie against the proletarians.
[ Bourgeois Socialists: ]
The second category consists of adherents of present-day society who have been frightened for its
future by the evils to which it necessarily gives rise. What they want, therefore, is to maintain this
society while getting rid of the evils which are an inherent part of it.
To this end, some propose mere welfare measures – while others come forward with grandiose
systems of reform which, under the pretense of re-organizing society, are in fact intended to
preserve the foundations, and hence the life, of existing society.
Communists must unremittingly struggle against these bourgeois socialists because they work for
the enemies of communists and protect the society which communists aim to overthrow.
[ Democratic Socialists: ]
Finally, the third category consists of democratic socialists who favor some of the same measures
the communists advocate, as described in Question 18, not as part of the transition to
communism, however, but as measures which they believe will be sufficient to abolish the misery
and evils of present-day society.
These democratic socialists are either proletarians who are not yet sufficiently clear about the
conditions of the liberation of their class, or they are representatives of the petty bourgeoisie, a
class which, prior to the achievement of democracy and the socialist measures to which it gives
rise, has many interests in common with the proletariat.
It follows that, in moments of action, the communists will have to come to an understanding with
these democratic socialists, and in general to follow as far as possible a common policy with them
– provided that these socialists do not enter into the service of the ruling bourgeoisie and attack
the communists.
It is clear that this form of co-operation in action does not exclude the discussion of differences.
– 25 –
What is the attitude of the communists to the
other political parties of our time?
This attitude is different in the different countries.
In England, France, and Belgium, where the bourgeoisie rules, the communists still have a
common interest with the various democratic parties, an interest which is all the greater the more
closely the socialistic measures they champion approach the aims of the communists – that is, the
more clearly and definitely they represent the interests of the proletariat and the more they depend
on the proletariat for support. In England, for example, the working-class Chartists10 are infinitely
closer to the communists than the democratic petty bourgeoisie or the so-called Radicals. 
54 Draft of a Communist Confession of Faith
In America, where a democratic constitution has already been established, the communists must
make the common cause with the party which will turn this constitution against the bourgeoisie
and use it in the interests of the proletariat – that is, with the agrarian National Reformers.
11
In Switzerland, the Radicals, though a very mixed party, are the only group with which the
communists can co-operate, and, among these Radicals, the Vaudois and Genevese are the most
advanced.
In Germany, finally, the decisive struggle now on the order of the day is that between the
bourgeoisie and the absolute monarchy. Since the communists cannot enter upon the decisive
struggle between themselves and the bourgeoisie until the bourgeoisie is in power, it follows that
it is in the interest of the communists to help the bourgeoisie to power as soon as possible in order
the sooner to be able to overthrow it. Against the governments, therefore, the communists must
continually support the radical liberal party, taking care to avoid the self-deceptions of the
bourgeoisie and not fall for the enticing promises of benefits which a victory for the bourgeoisie
would allegedly bring to the proletariat. The sole advantages which the proletariat would derive
from a bourgeois victory would consist
(i) in various concessions which would facilitate the unification of the proletariat
into a closely knit, battle-worthy, and organized class; and
(ii) in the certainly that, on the very day the absolute monarchies fall, the struggle
between bourgeoisie and proletariat will start. From that day on, the policy of the
communists will be the same as it now is in the countries where the bourgeoisie is
already in power. 
Demands of the Communist Party in Germany
“Demands of the Communist Party in Germany” were written by Karl Marx and Frederick Engels in
Paris between March 21 (when Engels arrived in Paris from Brussels) and March 24, 1848. This
document was discussed by members of the Central Authority, who approved and signed it as the.
political programme of the Communist League in the revolution that broke out in Germany. In March
it was printed as a leaflet, for distribution among revolutionary German emigrant workers who were
about to return home. Austrian and German diplomats in Paris informed their respective governments
about this as early as March 27, 28 and 29. (The Austrian Ambassador enclosed in his letter a copy of
the leaflet which he dated “March 25”.) The leaflet soon reached members of the Communist League
in other countries, in particular, German emigrant workers in London.
Early in April, the “Demands of the Communist Party in Germany” were published in such German
democratic papers as Berliner Zeitungs-Halle (special supplement to No. 82, April 5, 1848),
Düsseldorfer Zeitung (No. 96, April 5, 1848), Mannheimer Abendzeitung (No. 96, April 6, 1848),
Trier’sche Zeitung (No. 97, April 6, 1848, supplement), Deutsche Allgemeine Zeitung (No. 100, April
9, 1848, supplement), and Zeitung für das deutsche Volk (No. 2 1, April 9, 1848).
Marx and Engels, who left for Germany round about April 6 and some time later settled in Cologne,
did their best along with their followers to popularise this programme document during the revolution.
In 1848 and 1849 it was repeatedly published in the periodical press and in leaflet form. Not later than
September 10, 1848, the “Demands” were printed in Cologne as a leaflet for circulation by the
Cologne Workers’ Association both in the town itself and in a number of districts of Rhenish Prussia.
In addition to minor stylistic changes, point 10 in the text of the leaflet was worded differently from
that published in March-April 1848. At the Second Democratic Congress held in Berlin in October
1848, Friedrich Beust, delegate from the Cologne Workers’ Association, spoke, on behalf of the social
question commission, in favour of adopting a programme of action closely following the “Demands”.
In November and December 1848, various points of the “Demands” were discussed at meetings of the
Cologne Workers’ Association. Many editions of the “Demands” published during the revolution and
after its defeat have survived to this day in their original form, some of them as copies kept in the
police archives.
At the end of 1848 or the beginning of 1849 an abridged version of the “Demands” was published in
pamphlet form by Weller Publishers in Leipzig. The slogan at the beginning of the document, the
second paragraph of point 9 and the last sentence of point 10 were omitted, and the words “The
Committee” were not included among the signatories. In 1853, an abridged version of the “Demands”
was printed, together with other documents of the Communist League, in the first part of the book Die
Communisten-Verschworungen des neunzehnten Jahrhunderts published in Berlin for purposes of
information by Wermuth and Stieber, two police officials, who staged a trial against the Communists
in Cologne in 1852. Later Engels reproduced the main points of the “Demands” in his essay On the
History of the Communist League, published in November 1885 in the newspaper Sozialdemokrat, and
as an introduction to the pamphlet: K. Marx, Enthüllungen über den Kommunisten Prozess zu Köln,
Hottingen-Zürich, 1885.
English translations of the “Demands of the Communist Party in Germany” appeared in the
collections: The Communist Manifesto of Karl Marx and Friedrich Engels with an introduction and
explanatory notes by D. Ryazanoff, Martin Lawrence, London (1930); K. Marx, Selected Works, Vol.
II, ed. V. Adoratsky, Moscow-Leningrad, Co-operative Publishing Society of Foreign Workers in the
USSR (1936); ibid., New York (1 936); Birth of the Communist Manifesto, edited and annotated, with
an Introduction by D. J. Struik, International Publishers, New York, 197 1, and in other publications.
56 Demands of the Communist Party in Germany
Demands of the Communist Party in Germany
“Workers of all countries, unite!”
1. The whole of Germany shall be declared a single and indivisible republic.
2. Every German, having reached the age of 21, shall have the right to vote and to be elected,
provided he has not been convicted of a criminal offence.
3. Representatives of the people shall receive payment so that workers, too, shall be able to
become members of the German parliament.
4. Universal arming of the people. In future the armies shall be simultaneously labour armies, so
that the troops shall not, as formerly, merely consume, but shall produce more than is necessary
for their upkeep.
This will moreover be conducive to the organisation of labour.
5. Legal services shall be free of charge.
6. All feudal obligations, dues, corvées, tithes etc., which have hitherto weighed upon the rural
population, shall be abolished without compensation.
7. Princely and other feudal estates, together with mines, pits, and so forth, shall become the
property of the state. The estates shall be cultivated on a large scale and with the most up-to-date
scientific devices in the interests of the whole of society.
8. Mortgages on peasant lands shall be declared the property of the state. Interest on such
mortgages shall be paid by the peasants to the state.
9. In localities where the tenant system is developed, the land rent or the quit-rent shall be paid to
the state as a tax.
The measures specified in Nos. 6, 7, 8 and 9 are to be adopted in order to reduce the communal
and other burdens hitherto imposed upon the peasants and small tenant farmers without curtailing
the means available for defraying state expenses and without imperilling production.
The landowner in the strict sense, who is neither a peasant nor a tenant farmer, has no share in
production. Consumption on his part is, therefore, nothing but abuse.
10. A state bank, whose paper issues are legal tender, shall replace all private banks.
This measure will make it possible to regulate the credit system in the interest of the people as a
whole, and will thus undermine the dominion of the big financial magnates. Further, by gradually
substituting paper money for gold and silver coin, the universal means of exchange (that
indispensable prerequisite of bourgeois trade and commerce) will be cheapened, and gold and
silver will be set free for use in foreign trade. Finally, this measure is necessary in order to bind
the interests of the conservative bourgeoisie to the Government.
11. All the means of transport, railways, canals, steamships, roads, the posts etc. shall be taken
over by the state. They shall become the property of the state and shall be placed free at the
disposal of the impecunious classes.
12. All civil servants shall receive the same salary, the only exception being that civil servants
who have a family to support and who therefore have greater requirements, shall receive a higher
salary.
13. Complete separation of Church and State. The clergy of every denomination shall be paid
only by the voluntary contributions of their congregations.
14. The right of inheritance to be curtailed.
57 Demands of the Communist Party in Germany
15. The introduction of steeply graduated taxes, and the abolition of taxes on articles of
consumption.
16. Inauguration of national workshops. The state guarantees a livelihood to all workers and
provides for those who are incapacitated for work.
17. Universal and free education of the people.
It is to the interest of the German proletariat, the petty bourgeoisie and the small peasants to
support these demands with all possible energy. Only by the realisation of these demands will the
millions in Germany, who have hitherto been exploited by a handful of persons and whom the
exploiters would like to keep in further subjection, win the rights and attain to that power to
which they are entitled as the producers of all wealth.
The Committee
Karl Marx, Karl Schapper, H. Bauer, F. Engels, J. Moll, W. Wolff
The Paris Commune. Address to the International Workingmen’s Association, May 1871
The “Paris Commune” was composed by Karl Marx as an address to the General Council of the
International, and included in a book, “The Civil War in France,” with the aim of distributing to
workers of all countries a clear understanding of the character and world-wide significance of the
heroic struggle of the Communards and their historical experience to learn from. The book was widely
circulated by 1872 it was translated into several languages and published throughout Europe and the
United States.
The first address was delivered on July 23rd, 1870, five days after the beginning of the FrancoPrussian War. The second address, delivered on September 9, 1870, gave a historical overview of the
events a week after the army of Bonaparte was defeated. The third address, delivered on May 30,
1871, two days after the defeat of the Paris Commune – detailed the significance and the underlining
causes of the first workers government ever created.
The Civil War in France was originally published by Marx as only the third address, only the first
half of which is reproduced here. In 1891, on the 20th anniversary of the Paris Commune, Engels
put together a new collection of the work. Engels decided to include the first two addresses that
Marx made to the International.
The Address is included here because it can be regarded as an amendment to the Manifesto,
clarifying a number of issues relating to the state based on the experience of the Commune.
On the dawn of March 18, Paris arose to the thunder-burst of “Vive la Commune!” What is the
Commune, that sphinx so tantalizing to the bourgeois mind?
“The proletarians of Paris,” said the Central Committee in its manifesto of March 18, “amidst the
failures and treasons of the ruling classes, have understood that the hour has struck for them to
save the situation by taking into their own hands the direction of public affairs.... They have
understood that it is their imperious duty, and their absolute right, to render themselves masters of
their own destinies, by seizing upon the governmental power.”
But the working class cannot simply lay hold of the ready-made state machinery, and wield
it for its own purposes.
The centralized state power, with its ubiquitous organs of standing army, police, bureaucracy,
clergy, and judicature – organs wrought after the plan of a systematic and hierarchic division of
labor – originates from the days of absolute monarchy, serving nascent bourgeois society as a
mighty weapon in its struggle against feudalism. Still, its development remained clogged by all
manner of medieval rubbish, seignorial rights, local privileges, municipal and guild monopolies,
and provincial constitutions. The gigantic broom of the French Revolution of the 18th century
swept away all these relics of bygone times, thus clearing simultaneously the social soil of its last
hindrances to the superstructure of the modern state edifice raised under the First Empire, itself
the offspring of the coalition wars of old semi-feudal Europe against modern France.
During the subsequent regimes, the government, placed under parliamentary control – that is,
under the direct control of the propertied classes – became not only a hotbed of huge national
debts and crushing taxes; with its irresistible allurements of place, pelf, and patronage, it became
not only the bone of contention between the rival factions and adventurers of the ruling classes;
but its political character changed simultaneously with the economic changes of society. At the
same pace at which the progress of modern industry developed, widened, intensified the class
antagonism between capital and labor, the state power assumed more and more the character of
the national power of capital over labor, of a public force organized for social enslavement, of an
engine of class despotism. 
59 Third Address to the International Working Men’s Association, May 1871
After every revolution marking a progressive phase in the class struggle, the purely repressive
character of the state power stands out in bolder and bolder relief. The Revolution of 1830,
resulting in the transfer of government from the landlords to the capitalists, transferred it from the
more remote to the more direct antagonists of the working men. The bourgeois republicans, who,
in the name of the February Revolution, took the state power, used it for the June [1848]
massacres, in order to convince the working class that “social” republic means the republic
entrusting their social subjection, and in order to convince the royalist bulk of the bourgeois and
landlord class that they might safely leave the cares and emoluments of government to the
bourgeois “republicans.”
However, after their one heroic exploit of June, the bourgeois republicans had, from the front, to
fall back to the rear of the “Party of Order” – a combination formed by all the rival fractions and
factions of the appropriating classes. The proper form of their joint-stock government was the
parliamentary republic, with Louis Bonaparte for its president. Theirs was a regime of avowed
class terrorism and deliberate insult towards the “vile multitude.”
If the parliamentary republic, as M. Thiers said, “divided them [the different fractions of the
ruling class] least,” it opened an abyss between that class and the whole body of society outside
their spare ranks. The restraints by which their own divisions had under former regimes still
checked the state power, were removed by their union; and in view of the threatening upheaval of
the proletariat, they now used that state power mercilessly and ostentatiously as the national war
engine of capital against labor.
In their uninterrupted crusade against the producing masses, they were, however, bound not only
to invest the executive with continually increased powers of repression, but at the same time to
divest their own parliamentary stronghold – the National Assembly – one by one, of all its own
means of defence against the Executive. The Executive, in the person of Louis Bonaparte, turned
them out. The natural offspring of the “Party of Order” republic was the Second Empire.
The empire, with the coup d’état for its birth certificate, universal suffrage for its sanction, and
the sword for its sceptre, professed to rest upon the peasantry, the large mass of producers not
directly involved in the struggle of capital and labor. It professed to save the working class by
breaking down parliamentarism, and, with it, the undisguised subserviency of government to the
propertied classes. It professed to save the propertied classes by upholding their economic
supremacy over the working class; and, finally, it professed to unite all classes by reviving for all
the chimera of national glory.
In reality, it was the only form of government possible at a time when the bourgeoisie had already
lost, and the working class had not yet acquired, the faculty of ruling the nation. It was acclaimed
throughout the world as the savior of society. Under its sway, bourgeois society, freed from
political cares, attained a development unexpected even by itself. Its industry and commerce
expanded to colossal dimensions; financial swindling celebrated cosmopolitan orgies; the misery
of the masses was set off by a shameless display of gorgeous, meretricious and debased luxury.
The state power, apparently soaring high above society and the very hotbed of all its corruptions.
Its own rottenness, and the rottenness of the society it had saved, were laid bare by the bayonet of
Prussia, herself eagerly bent upon transferring the supreme seat of that regime from Paris to
Berlin. Imperialism is, at the same time, the most prostitute and the ultimate form of the state
power which nascent bourgeois society had commenced to elaborate as a means of its own
emancipation from feudalism, and which full-grown bourgeois society had finally transformed
into a means for the enslavement of labor by capital.
The direct antithesis to the empire was the Commune. The cry of “social republic,” with which
the February [1848] Revolution was ushered in by the Paris proletariat, did but express a vague
aspiration after a republic that was not only to supercede the monarchical form of class rule, but
class rule itself. The Commune was the positive form of that republic. 
60 Third Address to the International Working Men’s Association, May 1871
Paris, the central seat of the old governmental power, and, at the same time, the social stronghold
of the French working class, had risen in arms against the attempt of Thiers and the Rurals to
restore and perpetuate that old governmental power bequeathed to them by the empire. Paris
could resist only because, in consequence of the siege, it had got rid of the army, and replaced it
by a National Guard, the bulk of which consisted of working men. This fact was now to be
transformed into an institution. The first decree of the Commune, therefore, was the suppression
of the standing army, and the substitution for it of the armed people.
The Commune was formed of the municipal councillors, chosen by universal suffrage in the
various wards of the town, responsible and revocable at short terms. The majority of its members
were naturally working men, or acknowledged representatives of the working class. The
Commune was to be a working, not a parliamentary body, executive and legislative at the same
time.
Instead of continuing to be the agent of the Central Government, the police was at once stripped
of its political attributes, and turned into the responsible, and at all times revocable, agent of the
Commune. So were the officials of all other branches of the administration. From the members of
the Commune downwards, the public service had to be done at workman’s wage. The vested
interests and the representation allowances of the high dignitaries of state disappeared along with
the high dignitaries themselves. Public functions ceased to be the private property of the tools of
the Central Government. Not only municipal administration, but the whole initiative hitherto
exercised by the state was laid into the hands of the Commune.
Having once got rid of the standing army and the police – the physical force elements of the old
government – the Commune was anxious to break the spiritual force of repression, the “parsonpower,” by the disestablishment and disendowment of all churches as proprietary bodies. The
priests were sent back to the recesses of private life, there to feed upon the alms of the faithful in
imitation of their predecessors, the apostles.
The whole of the educational institutions were opened to the people gratuitously, and at the same
time cleared of all interference of church and state. Thus, not only was education made accessible
to all, but science itself freed from the fetters which class prejudice and governmental force had
imposed upon it.
The judicial functionaries were to be divested of that sham independence which had but served to
mask their abject subserviency to all succeeding governments to which, in turn, they had taken,
and broken, the oaths of allegiance. Like the rest of public servants, magistrates and judges were
to be elective, responsible, and revocable.
The Paris Commune was, of course, to serve as a model to all the great industrial centres of
France. The communal regime once established in Paris and the secondary centres, the old
centralized government would in the provinces, too, have to give way to the self-government of
the producers.
In a rough sketch of national organisation, which the Commune had no time to develop, it states
clearly that the Commune was to be the political form of even the smallest country hamlet, and
that in the rural districts the standing army was to be replaced by a national militia, with an
extremely short term of service. The rural communities of every district were to administer their
common affairs by an assembly of delegates in the central town, and these district assemblies
were again to send deputies to the National Delegation in Paris, each delegate to be at any time
revocable and bound by the mandat imperatif (formal instructions) of his constituents. The few
but important functions which would still remain for a central government were not to be
suppressed, as has been intentionally misstated, but were to be discharged by Communal and
thereafter responsible agents.
The unity of the nation was not to be broken, but, on the contrary, to be organized by Communal
Constitution, and to become a reality by the destruction of the state power which claimed to be 
61 Third Address to the International Working Men’s Association, May 1871
the embodiment of that unity independent of, and superior to, the nation itself, from which it was
but a parasitic excrescence.
While the merely repressive organs of the old governmental power were to be amputated, its
legitimate functions were to be wrested from an authority usurping pre-eminence over society
itself, and restored to the responsible agents of society. Instead of deciding once in three or six
years which member of the ruling class was to misrepresent the people in Parliament, universal
suffrage was to serve the people, constituted in Communes, as individual suffrage serves every
other employer in the search for the workmen and managers in his business. And it is well-known
that companies, like individuals, in matters of real business generally know how to put the right
man in the right place, and, if they for once make a mistake, to redress it promptly. On the other
hand, nothing could be more foreign to the spirit of the Commune than to supercede universal
suffrage by hierarchical investiture.12
It is generally the fate of completely new historical creations to be mistaken for the counterparts
of older, and even defunct, forms of social life, to which they may bear a certain likeness. Thus,
this new Commune, which breaks with the modern state power, has been mistaken for a
reproduction of the medieval Communes, which first preceded, and afterward became the
substratum of, that very state power. The Communal Constitution has been mistaken for an
attempt to break up into the federation of small states, as dreamt of by Montesquieu and the
Girondins13, that unity of great nations which, if originally brought about by political force, has
now become a powerful coefficient of social production. The antagonism of the Commune
against the state power has been mistaken for an exaggerated form of the ancient struggle against
over-centralization. Peculiar historical circumstances may have prevented the classical
development, as in France, of the bourgeois form of government, and may have allowed, as in
England, to complete the great central state organs by corrupt vestries, jobbing councillors, and
ferocious poor-law guardians in the towns, and virtually hereditary magistrates in the counties.
The Communal Constitution would have restored to the social body all the forces hitherto
absorbed by the state parasite feeding upon, and clogging the free movement of, society. By this
one act, it would have initiated the regeneration of France.
The provincial French bourgeois saw in the Commune an attempt to restore the sway their order
had held over the country under Louis Philippe, and which, under Louis Napoleon, was
supplanted by the pretended rule of the country over the towns. In reality, the Communal
Constitution brought the rural producers under the intellectual lead of the central towns of their
districts, and there secured to them, in the working men, the natural trustees of their interests. The
very existence of the Commune involved, as a matter of course, local municipal liberty, but no
longer as a check upon the now superseded state power. It could only enter into the head of a
Bismarck – who, when not engaged on his intrigues of blood and iron, always likes to resume his
old trade, so befitting his mental calibre, of contributor to Kladderadatsch (the Berlin Punch14) –
it could only enter into such a head to ascribe to the Paris Commune aspirations after the
caricature of the old French municipal organization of 1791, the Prussian municipal constitution
which degrades the town governments to mere secondary wheels in the police machinery of the
Prussian state. The Commune made that catchword of bourgeois revolutions – cheap government
– a reality by destroying the two greatest sources of expenditure: the standing army and state
functionarism. Its very existence presupposed the non-existence of monarchy, which, in Europe at
least, is the normal encumbrance and indispensable cloak of class rule. It supplied the republic
with the basis of really democratic institutions. But neither cheap government nor the “true
republic” was its ultimate aim; they were its mere concomitants.
The multiplicity of interpretations to which the Commune has been subjected, and the multiplicity
of interests which construed it in their favor, show that it was a thoroughly expansive political
form, while all the previous forms of government had been emphatically repressive. Its true secret
was this: It was essentially a working class government, the product of the struggle of the 
62 Third Address to the International Working Men’s Association, May 1871
producing against the appropriating class, the political form at last discovered under which to
work out the economical emancipation of labor.
Except on this last condition, the Communal Constitution would have been an impossibility and a
delusion. The political rule of the producer cannot co-exist with the perpetuation of his social
slavery. The Commune was therefore to serve as a lever for uprooting the economical foundation
upon which rests the existence of classes, and therefore of class rule. With labor emancipated,
every man becomes a working man, and productive labor ceases to be a class attribute.
It is a strange fact. In spite of all the tall talk and all the immense literature, for the last 60 years,
about emancipation of labor, no sooner do the working men anywhere take the subject into their
own hands with a will, than uprises at once all the apologetic phraseology of the mouthpieces of
present society with its two poles of capital and wage-slavery (the landlord now is but the
sleeping partner of the capitalist), as if the capitalist society was still in its purest state of virgin
innocence, with its antagonisms still undeveloped, with its delusions still unexploded, with its
prostitute realities not yet laid bare. The Commune, they exclaim, intends to abolish property, the
basis of all civilization!
Yes, gentlemen, the Commune intended to abolish that class property which makes the labor of
the many the wealth of the few. It aimed at the expropriation of the expropriators. It wanted to
make individual property a truth by transforming the means of production, land, and capital, now
chiefly the means of enslaving and exploiting labor, into mere instruments of free and associated
labor. But this is communism, “impossible” communism! Why, those member of the ruling
classes who are intelligent enough to perceive the impossibility of continuing the present system
– and they are many – have become the obtrusive and full-mouthed apostles of co-operative
production. If co-operative production is not to remain a sham and a snare; if it is to supersede the
capitalist system; if united co-operative societies are to regulate national production upon
common plan, thus taking it under their own control, and putting an end to the constant anarchy
and periodical convulsions which are the fatality of capitalist production – what else, gentlemen,
would it be but communism, “possible” communism?
The working class did not expect miracles from the Commune. They have no ready-made utopias
to introduce par decret du peuple. They know that in order to work out their own emancipation,
and along with it that higher form to which present society is irresistibly tending by its own
economical agencies, they will have to pass through long struggles, through a series of historic
processes, transforming circumstances and men. They have no ideals to realize, but to set free the
elements of the new society with which old collapsing bourgeois society itself is pregnant. In the
full consciousness of their historic mission, and with the heroic resolve to act up to it, the working
class can afford to smile at the coarse invective of the gentlemen’s gentlemen with pen and
inkhorn, and at the didactic patronage of well-wishing bourgeois-doctrinaires, pouring forth their
ignorant platitudes and sectarian crotchets in the oracular tone of scientific infallibility.
When the Paris Commune took the management of the revolution in its own hands; when plain
working men for the first time dared to infringe upon the governmental privilege of their “natural
superiors,” and, under circumstances of unexampled difficulty, performed it at salaries the highest
of which barely amounted to one-fifth what, according to high scientific authority*
, is the
minimum required for a secretary to a certain metropolitan school-board – the old world writhed
in convulsions of rage at the sight of the Red Flag, the symbol of the Republic of Labor, floating
over the Hôtel de Ville.
And yet, this was the first revolution in which the working class was openly acknowledged as the
only class capable of social initiative, even by the great bulk of the Paris bourgeois –
shopkeepers, tradesmen, merchants – the wealthy capitalist alone excepted. The Commune had
 * Professor Huxley. [Note to the German addition of 1871.]
63 Third Address to the International Working Men’s Association, May 1871
saved them by a sagacious settlement of that ever recurring cause of dispute among the bourgeois
themselves – the debtor and creditor accounts.15 The same portion of the bourgeois, after they had
assisted in putting down the working men’s insurrection of June 1848, had been at once
unceremoniously sacrificed to their creditors16 by the then Constituent Assembly. But this was
not their only motive for now rallying around the working class. They felt there was but one
alternative – the Commune, or the empire – under whatever name it might reappear. The empire
had ruined them economically by the havoc it made of public wealth, by the wholesale financial
swindling it fostered, by the props it lent to the artificially accelerated centralization of capital,
and the concomitant expropriation of their own ranks. It had suppressed them politically, it had
shocked them morally by its orgies, it had insulted their Voltairianism by handing over the
education of their children to the fréres Ignorantins,
17 it had revolted their national feeling as
Frenchmen by precipitating them headlong into a war which left only one equivalent for the ruins
it made – the disappearance of the empire. In fact, after the exodus from Paris of the high
Bonapartist and capitalist boheme, the true bourgeois Party of Order came out in the shape of the
“Union Republicaine,”18 enrolling themselves under the colors of the Commune and defending it
against the wilful misconstructions of Thiers. Whether the gratitude of this great body of the
bourgeois will stand the present severe trial, time must show.
The Commune was perfectly right in telling the peasants that “its victory was their only hope.” Of
all the lies hatched at Versailles and re-echoed by the glorious European penny-a-liner, one of the
most tremendous was that the Rurals represented the French peasantry. Think only of the love of
the French peasant for the men to whom, after 1815, he had to pay the milliard indemnity.19 In the
eyes of the French peasant, the very existence of a great landed proprietor is in itself an
encroachment on his conquests of 1789. The bourgeois, in 1848, had burdened his plot of land
with the additional tax of 45 cents, in the franc; but then he did so in the name of the revolution;
while now he had fomented a civil war against revolution, to shift on to the peasant’s shoulders
the chief load of the 5 milliards of indemnity to be paid to the Prussian. The Commune, on the
other hand, in one of its first proclamations, declared that the true originators of the war would be
made to pay its cost. The Commune would have delivered the peasant of the blood tax – would
have given him a cheap government – transformed his present blood-suckers, the notary,
advocate, executor, and other judicial vampires, into salaried communal agents, elected by, and
responsible to, himself. It would have freed him of the tyranny of the garde champetre, the
gendarme, and the prefect; would have put enlightenment by the schoolmaster in the place of
stultification by the priest. And the French peasant is, above all, a man of reckoning. He would
find it extremely reasonable that the pay of the priest, instead of being extorted by the taxgatherer, should only depend upon the spontaneous action of the parishioners’ religious instinct.
Such were the great immediate boons which the rule of the Commune – and that rule alone – held
out to the French peasantry. It is, therefore, quite superfluous here to expatiate upon the more
complicated but vital problems which the Commune alone was able, and at the same time
compelled, to solve in favor of the peasant – viz., the hypothecary debt, lying like an incubus
upon his parcel of soil, the prolétariat foncier (the rural proletariat), daily growing upon it, and
his expropriation from it enforced, at a more and more rapid rate, by the very development of
modern agriculture and the competition of capitalist farming.
The French peasant had elected Louis Bonaparte president of the republic; but the Party of Order
created the empire. What the French peasant really wants he commenced to show in 1849 and
1850, by opposing his maire to the government’s prefect, his school-master to the government’s
priest, and himself to the government’s gendarme. All the laws made by the Party of Order in
January and February 1850 were avowed measures of repression against the peasant. The peasant
was a Bonapartist, because the Great Revolution, with all its benefits to him, was, in his eyes,
personified in Napoleon. This delusion, rapidly breaking down under the Second Empire (and in 
64 Third Address to the International Working Men’s Association, May 1871
its very nature hostile to the Rurals), this prejudice of the past, how could it have withstood the
appeal of the Commune to the living interests and urgent wants of the peasantry?
The Rurals – this was, in fact, their chief apprehension – knew that three months’ free
communication of Communal Paris with the provinces would bring about a general rising of the
peasants, and hence their anxiety to establish a police blockade around Paris, so as to stop the
spread of the rinderpest [cattle pest – contagious disease].
If the Commune was thus the true representative of all the healthy elements of French society,
and therefore the truly national government, it was, at the same time, as a working men’s
government, as the bold champion of the emancipation of labor, emphatically international.
Within sight of that Prussian army, that had annexed to Germany two French provinces, the
Commune annexed to France the working people all over the world.
The Second Empire had been the jubilee of cosmopolitan blackleggism, the rakes of all countries
rushing in at its call for a share in its orgies and in the plunder of the French people. Even at this
moment, the right hand of Thiers is Ganessco, the foul Wallachian, and his left hand is
Markovsky, the Russian spy. The Commune admitted all foreigners to the honor of dying for an
immortal cause. Between the foreign war lost by their treason, and the civil war fomented by their
conspiracy with the foreign invader, the bourgeoisie had found the time to display their patriotism
by organizing police hunts upon the Germans in France. The Commune made a German working
man [Leo Frankel] its Minister of Labor. Thiers, the bourgeoisie, the Second Empire, had
continually deluded Poland by loud professions of sympathy, while in reality betraying her to,
and doing the dirty work of, Russia. The Commune honoured the heroic sons of Poland [J.
Dabrowski and W. Wróblewski] by placing them at the head of the defenders of Paris. And, to
broadly mark the new era of history it was conscious of initiating, under the eyes of the
conquering Prussians on one side, and the Bonapartist army, led by Bonapartist generals, on the
other, the Commune pulled down that colossal symbol of martial glory, the Vendôme Column.20
The great social measure of the Commune was its own working existence. Its special measures
could but betoken the tendency of a government of the people by the people. Such were the
abolition of the nightwork of journeymen bakers; the prohibition, under penalty, of the
employers’ practice to reduce wages by levying upon their workpeople fines under manifold
pretexts – a process in which the employer combines in his own person the parts of legislator,
judge, and executor, and filches the money to boot. Another measure of this class was the
surrender to associations of workmen, under reserve of compensation, of all closed workshops
and factories, no matter whether the respective capitalists had absconded or preferred to strike
work.
The financial measures of the Commune, remarkable for their sagacity and moderation, could
only be such as were compatible with the state of a besieged town. Considering the colossal
robberies committed upon the city of Paris by the great financial companies and contractors,
under the protection of Haussman,21 the Commune would have had an incomparably better title to
confiscate their property than Louis Napoleon had against the Orleans family. The Hohenzollern
and the English oligarchs, who both have derived a good deal of their estates from church
plunders, were, of course, greatly shocked at the Commune clearing but 8,000f out of
secularization.
While the Versailles government, as soon as it had recovered some spirit and strength, used the
most violent means against the Commune; while it put down the free expression of opinion all
over France, even to the forbidding of meetings of delegates from the large towns; while it
subjected Versailles and the rest of France to an espionage far surpassing that of the Second
Empire; while it burned by its gendarme inquisitors all papers printed at Paris, and sifted all
correspondence from and to Paris; while in the National Assembly the most timid attempts to put
in a word for Paris were howled down in a manner unknown even to the Chambre introuvable of 
65 Third Address to the International Working Men’s Association, May 1871
1816; with the savage warfare of Versailles outside, and its attempts at corruption and conspiracy
inside Paris – would the Commune not have shamefully betrayed its trust by affecting to keep all
the decencies and appearances of liberalism as in a time of profound peace? Had the government
of the Commune been akin to that of M. Thiers, there would have been no more occasion to
suppress Party of Order papers at Paris that there was to suppress Communal papers at Versailles.
It was irritating indeed to the Rurals that at the very same time they declared the return to the
church to be the only means of salvation for France, the infidel Commune unearthed the peculiar
mysteries of the Picpus nunnery22, and of the Church of St. Laurent. It was a satire upon M.
Thiers that, while he showered grand crosses upon the Bonapartist generals in acknowledgment
of their mastery in losing battles, singing capitulations, and turning cigarettes at Wilhelmshöhe,23
the Commune dismissed and arrested its generals whenever they were suspected of neglecting
their duties. The expulsion from, and arrest by, the Commune of one of its members [Blanchet]
who had slipped in under a false name, and had undergone at Lyons six days’ imprisonment for
simple bankruptcy, was it not a deliberate insult hurled at the forger, Jules Favre, then still the
foreign minister of France, still selling France to Bismarck, and still dictating his orders to that
paragon government of Belgium? But indeed the Commune did not pretend to infallibility, the
invariable attribute of all governments of the old stamp. It published its doings and sayings, it
initiated the public into all its shortcomings.
In every revolution there intrude, at the side of its true agents, men of different stamp; some of
them survivors of and devotees to past revolutions, without insight into the present movement,
but preserving popular influence by their known honesty and courage, or by the sheer force of
tradition; others mere brawlers who, by dint of repeating year after year the same set of
stereotyped declarations against the government of the day, have sneaked into the reputation of
revolutionists of the first water. After March 18, some such men did also turn up, and in some
cases contrived to play pre-eminent parts. As far as their power went, they hampered the real
action of the working class, exactly as men of that sort have hampered the full development of
every previous revolution. They are an unavoidable evil: with time they are shaken off; but time
was not allowed to the Commune.
Wonderful, indeed, was the change the Commune had wrought in Paris! No longer any trace of
the tawdry Paris of the Second Empire! No longer was Paris the rendezvous of British landlords,
Irish absentees, 24 American ex-slaveholders and shoddy men, Russian ex-serfowners, and
Wallachian boyards. No more corpses at the morgue, no nocturnal burglaries, scarcely any
robberies; in fact, for the first time since the days of February 1848, the streets of Paris were safe,
and that without any police of any kind.
“We,” said a member of the Commune, “hear no longer of assassination, theft, and personal
assault; it seems indeed as if the police had dragged along with it to Versailles all its Conservative
friends.”
The cocottes had refound the scent of their protectors – the absconding men of family, religion,
and, above all, of property. In their stead, the real women of Paris showed again at the surface –
heroic, noble, and devoted, like the women of antiquity. Working, thinking fighting, bleeding
Paris – almost forgetful, in its incubation of a new society, of the Cannibals at its gates – radiant
in the enthusiasm of its historic initiative!
Opposed to this new world at Paris, behold the old world at Versailles – that assembly of the
ghouls of all defunct regimes, Legitimists and Orleanists, eager to feed upon the carcass of the
nation – with a tail of antediluvian republicans, sanctioning, by their presence in the Assembly,
the slaveholders’ rebellion, relying for the maintenance of their parliamentary republic upon the
vanity of the senile mountebank at its head, and caricaturing 1789 by holding their ghastly 
66 Third Address to the International Working Men’s Association, May 1871
meetings in the Jeu de Paume.
1 There it was, this Assembly, the representative of everything
dead in France, propped up to the semblance of life by nothing but the swords of the generals of
Louis Bonaparte. Paris all truth, Versailles all lie; and that lie vented through the mouth of Thiers.
Thiers tells a deputation of the mayors of the Seine-et-Oise – “You may rely upon my word,
which I have never broken!”
He tells the Assembly itself that “it was the most freely elected and most liberal Assembly France
ever possessed”; he tells his motley soldiery that it was “the admiration of the world, and the
finest army France ever possessed”; he tells the provinces that the bombardment of Paris by him
was a myth: “If some cannon-shots have been fired, it was not the deed of the army of Versailles,
but of some insurgents trying to make believe that they are fighting, while they dare not show
their faces.” He again tells the provinces that “the artillery of Versailles does not bombard Paris,
but only cannonades it.” He tells the Archbishop of Paris that the pretended executions and
reprisals (!) attributed to the Versailles troops were all moonshine. He tells Paris that he was only
anxious “to free it from the hideous tyrants who oppress it,” and that, in fact, the Paris of the
Commune was “but a handful of criminals.”
The Paris of M. Thiers was not the real Paris of the “vile multitude,” but a phantom Paris, the
Paris of the francs-fileurs,
25 the Paris of the Boulevards, male and female – the rich, the capitalist,
the gilded, the idle Paris, now thronging with its lackeys, its blacklegs, its literary bohome, and its
cocottes at Versailles, Saint-Denis, Rueil, and Saint-Germain; considering the civil war but an
agreeable diversion, eyeing the battle going on through telescopes, counting the rounds of
cannon, swearing by their own honour and that of their prostitutes, that the performance was far
better got up than it used to be at the Porte St. Martin. The men who fell were really dead; the
cries of the wounded were cries in good earnest; and, besides, the whole thing was so intensely
historical.
This is the Paris of M. Thiers, as the emigration of Coblenz was the France of M. de Calonne.26
 1 The tennis court where the National Assembly of 1789 adopted its famous decisions. [Note to the German addition of
1871.]
67 Third Address to the International Working Men’s Association, May 1871
Endnotes
1 The first Russian translation of the Manifesto of the Communist Party was made by Bakunin, who
despite being one of Marx and Engels’ most pronounced opponents in the working class movement,
saw the great revolutionary importance contained within the Manifesto. Published in Geneva in 1869
(printing it in Russia was impossible due to state censorship), Bakunin’ s translation was not
completely accurate, and was replaced a decade later by Plekhanov’s translation in 1882, for which
both Marx and Engels wrote a preface. 2 A reference to the events that occurred in Russia after the assassination, on March, 1, 1881, of
Emperor Alexander II by Narodnaya Volya members. Alexander III, his successor, was staying in
Gatchina for fear of further terrorism.
3 This preface was written by Engels on May 1, 1890, when, in accordance with the decision of the
Paris Congress of the Second International (July 1889), mass demonstrations, strikes and meetings
were held in numerous European and American countries. The workers put forward the demand for an
8 hour working day and other demands set forth by the Congress. From that day forward workers all
over the world celebrate the first of May as a day of international proletarian solidarity.
4 A reference to the movement for an electoral reform which, under the pressure of the working class,
was passed by the British House of Commons in 1831 and finally endorsed by the House of Lords in
June, 1832. The reform was directed against monopoly rule of the landed and finance aristocracy and
opened the way to Parliament for the representatives of the industrial bourgeoisie. Neither workers nor
the petty-bourgeois were allowed electoral rights, despite assurances they would.
5 The famous final phrase of the Manifesto, “Working Men of All Countries, Unite!”, in the original
German is: “Proletarier aller Länder, vereinigt euch!” Thus, a more correct translation would be
“Proletarians of all countries, Unite!”
“Workers of the World, Unite. You have nothing to lose but your chains!” is a popularisation of the
last three sentences, and is not found in any official translation. Since this English translation was
approved by Engels, we have kept the original intact.
6 In their works written in later periods, Marx and Engels substituted the more accurate concepts of
“sale of labour power”, “value of labour power” and “price of labour power” (first introduced by
Marx) for “sale of labour”, “value of labour” and “price of labour”, as used here.
7 Engels left half a page blank here in the manuscript. The “Draft of the Communist Confession of
Faith,” has the answer shown for the same question (Number 12).
8 Engels’ put “unchanged” here, referring to the answer in the June draft under No. 21 as shown.
9 Similarly, this refers to the answer to Question 23 in the June draft.
10 The Chartists were the participants in the political movement of the British workers which lasted
from the 1830s to the middle 1850s and had as its slogan the adoption of a People’s Charter,
demanding universal franchise and a series of conditions guaranteeing voting rights for all workers.
Lenin defined Chartism as the world’s “first broad, truly mass and politically organized proletarian
revolutionary movement” (Collected Works, Eng. ed., Progress Publishers, Moscow, 1965, Vol. 29, p.
309.) The decline of the Chartist movement was due to the strengthening of Britain’s industrial and
commercial monopoly and the bribing of the upper stratum of the working class (“the labour
aristocracy”) by the British bourgeoisie out of its super-profits. Both factors led to the strengthening of
opportunist tendencies in this stratum as expressed, in particular, by the refusal of the trade union
leaders to support Chartism.
11 Probably a references to the National Reform Association, founded during the 1840s by George H.
Evans, with headquarters in New York City, which had for its motto, “Vote Yourself a Farm”.
68 Third Address to the International Working Men’s Association, May 1871
12 A top-down system of appointing officials in bourgeois systems, where high-up officials appoint
many or all lower officials.
13 Girondins – The party of the influential bourgeoisie during the French revolution at the end of the
18th century. (The name is derived from the Department of Gironde.) It came out against the Jacobin
government and the revolutionary masses which supported it, under the banner of defending the
departments’ right to autonomy and federation.
14 The party of the influential bourgeoisie during the French revolution at the end of the 18th century.
(The name is derived from the Department of Gironde.) It came out against the Jacobin government
and the revolutionary masses which supported it, under the banner of defending the departments’ right
to autonomy and federation.
15 A reference to the Paris Commune’s decree of April 16, 1871, providing for payment of all debts in
instalments over three years and abolition of interest on them.
16 On Aug. 22, 1848, the Constituent Assembly rejected the bill on “amiable agreements” (concordats
á l’amiable) aimed to introduce the deferred payment of debts. As a result of this measure, a
considerable section of the petty-bourgeoisie were utterly ruined and found themselves completely
dependent on the creditors of the richest bourgeoisie.
17 Fréres Ignorantins – Ignorant Brothers, a nickname for a religious order, founded in Rheims in
1680, whose members pledged themselves to educate children of the poor. The pupils received a
predominantly religious education and barely any knowledge otherwise.
18 Alliance républicaine des Départements – a political association of petty-bourgeois representatives
from the various departments of France, who lived in Paris; calling on the people to fight against the
Versailles government and the monarchist National Assembly and to support the Commune
throughout the country.
19 The law of April 27, 1825 on the payment of compensation to the former émigrés for the landed
states confiscated from them during the preceding French Revolution.
20 The Vendôme Column was erected between 1806 and 1810 in Paris in honour of the victories of
Napoleonic France; it was made out of the bronze captured from enemy guns and was crowned by a
statue of Napoleon. On May 16, 1871, by order of the Paris Commune, the Vendôme Column was
pulled down.
21 During the Second Empire, Baron Haussmann was Prefect of the Department of the Seine (the City
of Paris). He introduced a number of changes in the layout of the city for the purpose of crushing
workers’ revolts.
22 In the Picpus nunnery cases of the nuns being incarcerated in cells for many years were exposed and
instruments of torture were found; in the church of St. Laurent a secret cemetery was found attesting
to the murders that had been committed there. These facts were exposed by the Commune’s
newspaper Mot d’Ordre on May 5, 1871, and in a pamphlet Les Crimes des congrégations religieuses.
23 The chief occupation of the French prisoners of war in Wilhelmshöhe (those captured after the
Battle of Sedan) was making cigars for their own use.
24 Rich landowners who hardly ever visited their estates, but instead had their land managed by agents
or leased it to petty-bourgeois who, in their turn, sub-leased the land at high rents.
25 Francs-fileurs – literally rendered: “free absconder,” the nickname given to the Paris bourgeois who
fled from the city during the siege. The name carried brazen historical irony as a result of its
resemblance to the word “francs-tireurs” (“free sharpshooters”) – French guerrillas who actively
fought against the Prussians.
26 A city in Germany; during the French Revolution at the end of the 18th-century it was the centre
where the landlord monarchist emigrés made preparations for intervention against revolutionary
France. Coblenz was the seat of the emigré government headed by the rabid reactionary de Calonne, a
former minister of Louis XVI.

```css
---
---

@import "{{ site.theme }}";

/* "row style" is flexible size and aligns pictures in center */
.row {
    align-items: center;
    display: flex;
  }
  
  /* "column style" is one-third of the width with padding */
  .column {
    flex: 33.33%;
    padding: 5px;
  }
```

