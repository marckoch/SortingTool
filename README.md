# Jetbrains Academy - Sorting Tool

My solutions for the Jetbrains Academy Problem Sorting Tool

https://hyperskill.org/projects/106

The solution is build up step by step over several stages. 
Stage 1 is the first and simple one. The following stages 
build up on the previous stages and get more and more advanced.
There are six stages in total.

Because each stage is completely independent of the previous one,
IntelliJ might show some warnings about duplicated code between 
the stages.

## Stage 1/6

[click here to see description @ JetBrains Academy](https://hyperskill.org/projects/106/stages/574/implement)

Basic analysis of the numbers that are entered.

just execute this:

    gradle -PmainClass=stage1.MainKt run --console=plain

    2 2 3 2 1 5 11
    
    Total numbers: 7
    The greatest number: 11 (1 time(s)).

## Stage 2/6

[click here to see description @ JetBrains Academy](https://hyperskill.org/projects/106/stages/575/implement)

We add a parameter to choose the analysis type: _word_, _line_ or _long_ 

just execute this:

    gradle -PmainClass=stage2.MainKt run --console=plain --args="-dataType line"
    # or
    gradle -PmainClass=stage2.MainKt run --console=plain --args="-dataType word"
    # or
    gradle -PmainClass=stage2.MainKt run --console=plain --args="-dataType long"

    2 2 3 4 5
    11 22
    2 1

    Total lines: 3.
    The longest line:
    2 2 3 4 5
    (1 time(s), 33%).

## Stage 3/6

[click here to see description @ JetBrains Academy](https://hyperskill.org/projects/106/stages/576/implement)

We add a feature to sort the given numbers.

just execute this:

    gradle -PmainClass=stage3.MainKt run --console=plain --args="-sortIntegers"

    2 3 4 1 2
    1 -23 5 6
    
    Total numbers: 9.
    Sorted data: -23 1 1 2 2 3 4 5 6

## Stage 4/6

[click here to see description @ JetBrains Academy](https://hyperskill.org/projects/106/stages/577/implement)

We add a feature to sort the given numbers. Parameter _sortingType_ can be _natural_ or _byCount_.

    usage: <script> -dataType [long|line|word] -sortingType [natural|byCount]

just execute this:

    gradle -PmainClass=stage4.MainKt run --console=plain --args="-dataType line -sortingType byCount"

    2 3 4
    2 2
    11 22 44 66
    121
    
    Total lines: 5.
    : 1 time(s), 20%
    11 22 44 66: 1 time(s), 20%
    121: 1 time(s), 20%
    2 2 : 1 time(s), 20%
    2 3 4: 1 time(s), 20%

## Stage 5/6

[click here to see description @ JetBrains Academy](https://hyperskill.org/projects/106/stages/578/implement)

We add error handling when arguments are wrong.

    usage: <script> -dataType [long|line|word] -sortingType [natural|byCount]

just execute this:

    gradle -PmainClass=stage5.MainKt run --console=plain --args="-dataType"

## Stage 6/6

[click here to see description @ JetBrains Academy](https://hyperskill.org/projects/106/stages/579/implement)

We can read and write input and output from and to a file.

    usage: <script> -dataType [long|line|word] -sortingType [natural|byCount] -inputFile input.txt -outputFile output.txt

just execute this:

    gradle -PmainClass=stage6.MainKt run --console=plain --args="-dataType line -sortingType byCount -inputFile ./src/main/resources/line_byCount.txt -output output.txt"

    Total lines: 5.
    bar: 1 time(s), 20%
    foo: 1 time(s), 20%
    test: 1 time(s), 20%
    blabla: 2 time(s), 40%
