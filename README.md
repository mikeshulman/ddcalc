Calculus, with differentials
============================

I hope that this will eventially be a collection of notes usable for teaching calculus with differentials and infinitesimals, with explicit emphasis on basic concepts of mathematics such as definitions, theorems, and problem solving (but very little emphasis on proofs).

My intention is to have three subdirectories "calc1", "calc2", and "calc3" containing notes appropriate for use in first, second, and third semester calculus respectively.  Roughly, this means that calc1 will treat one-variable differentials and derivatives, one-variable integration, and limits; calc2 will treat applications of integration, sequences and series, and differential equations; and calc3 will treat multivariable calculus primarily in 2 and 3 dimensions, including multiple integrals, partial derivatives, and vector calculus through Stokes' theorem.

There will also be a smaller set of "crash course" notes appropriate for use in a first complex analysis class, and potentially others.  I don't know whether differential forms would be useful in a first real analysis class, and in a differential geometry class they should probably be introduced in the usual way instead.  But there might be a role for a set of notes appropriate for more applied classes, such as E&M or relativity.

I intend to design each course under the assumption that students may have satisfied its prerequisites with a "traditional" calculus class (lacking differentials and infinitesimals), and likewise that they may leave it into a traditional class.  (Students who take the whole 1-2-3 sequence with differentials will be at an advantage, of course.)  This is in deference to the reality of the modern undergraduate teacher, who usually doesn't get to control a cohort of students through their entire calculus education, and is also often bound to a rigid syllabus.

Additionally, in view of the fact that an undergraduate teacher is often required to use a particular textbook, these notes will not be themselves a textbook.  Instead, my intent is for them to be usable to supplement any standard textbook.  I plan to indicate, for each course, in what sequence I would cover the topics, and where to insert each set of supplementary notes, perhaps with reference to particular chapters and sections of some common textbooks.  Since these notes are free and online, a teacher can easily add them to the students' reading without imposing on them any additional cost.  I also intend to use "semantic macros" in LaTeX as much as possible, so that a single modification can bring the notation in line with that of any particular other textbook.  (There are exceptions, however, such as places where the approach of differentials mandates the use or non-use of certain notation, or where I feel that some common notation is actively harmful and should be discouraged even if a textbook uses it.)

Because these notes are released under a Creative Commons BY-SA or BY-NC-SA license, it should be possible to mix them into any similarly licensed open calculus book to create a complete textbook.  I have chosen dual licensing for these notes to make this maximally possible, since some books may have one license and some the other.  I may create such a mix myself someday.

Organization and compilation
============================

Each set of notes is written with one "chapter" per LaTeX input file.  The intent is that each chapter would be a separate handout given to students.  With this in mind, each chapter file can be compiled individually.  However, each directory also contains a "master" file that includes all the chapter files, in case you want a monolithic output file.  A bit of LaTeX wizardry enables both the master file and the chapter files to be compiled individually, but requires a bit of help on your part.  If you are on a UNIX-compatible operating system, then run the `lnaux` script on each subdirectory that you intend to use, e.g.

    ~/ddcalc$ ./lnaux calc3

If you don't want to do this, or if your operating system doesn't support symbolic links, then you can instead add an extra command to your compilation of each chapter file.  E.g. to compile `forms.tex` in the `calc3` subdirectory, you'll need to say

    cp calc3.aux forms.aux && pdflatex forms

At some point, it might be worthwhile writing a Makefile that automates the latter.
