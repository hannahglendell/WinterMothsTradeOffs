---
editor_options: 
  markdown: 
    wrap: 72
---

# Repository structure

This repostory has four folders - data, figures, renv and scripts

-   data contains the raw data and clean data. Data cleaning performed
    in cleaning.Rmd found in scripts folder. Also contains some saved
    outputs from the structural equation modelling

-   figures - figures saved as .png

-   renv - all the R packages used in this repository

-   scripts - scripts for all analyses and for creating figures. First
    run the cleaning.Rmd to clean all the data. Then there are two
    folders

    -   Analysis

        -   Appendix - Ambient temperature contains code for calculating
            the life cycle dates of wild winter moths, and code for
            calculating the mean temperature in each treatment during
            'resource acquisition' and 'resource allocation' periods

        -   Experiment 1 - all code for experiment 1, including analysis
            on clutch size, egg size, their trade-off, and the SEM
            analysis

        -   Experiment 2 - all code for investigating the fitness
            effects of egg size on hatching success and larval growth
            rate.

    -   Making figures - code for making the figures saved in 'figures'
        folder

# Raw data files

## Experiment 1

**ambient thermologger.csv**

-   the temperature experienced by the outdoor ambient control group,
    recorded using a thermologger device.

-   contains two columns; datetime and temperature

**raw egg sizes.csv**

-   contains the individual measurements of the 3381 individual eggs
    measured from 381 photographs

-   columns include:

    -   clutch_code - randomised code assigned to the clutch photo, so
        that photos were measured blind to treatment information.

    -   egg_number - the number of the egg in that photograph

    -   area - size of individual egg in mm\^2

    -   mean_area - mean egg size of all 10 eggs measured from that
        photograph.

**mean egg sizes.csv**

-   contains the mean egg size of each clutch (381 cluches in total).
    Calculated as the mean of the ten individual egg measurements from
    each clutch, recorded in eggs raw egg sizes.csv

-   columns include:

    -   clutch_code - randomised code assigned to the clutch photo, so
        that photos were measured blind to treatment information.

    -   egg_mean_1A - mean eggs size in that clutch in mm\^2

    -   egg_mean_1B_same_set_of_10_eggs - mean egg size as measured from
        a second photo of the same set of 10 eggs from that clutch. Used
        to calculate repeatability of egg size measurements.

    -   egg_mean_2A_different_set_of_10_eggs - mean eggs sizes as
        measured from a photo of 10 different eggs from that clutch.
        Used to calculate repeatability of egg size measurements. -

    -   replacement_image - a small number of clutches had to have a
        second photograph taken when the quality of the first photograph
        was too poor to measure egg size - notes

**emergence_egg_counts(Sheet1).csv**

-   contains the counts of eggs from each clutch. counts are split into
    green eggs (infertile), orange eggs (fertile), and total clutch_size

-   columns include:

    -   pupal_treatment - meaning resource allocation temperature
        treatment

    -   emergence_date - date of adult emerging from pupa -

    -   sex -

    -   adultID

    -   weight

    -   mateID

    -   treatment_coombination - redundant column used for matching
        females to a male mate within the same treatment column

    -   clutchID

    -   notes

    -   age_at_photo - redundant column. Adult winter moths were
        photographed for a different experiment

    -   uploaded - redundant column used for different experiment

    -   dead - used to note that the adult moth had died

    -   green_eggs - number of green eggs in that clutch

    -   orange_eggs - number of orange eggs in that clutch

    -   clutch_size - total clutch size of green + orange eggs

    -   eggs_photographed - used to note that eggs had been photographed
        for measuring egg size

    -   clutch_code - random number code assigned to each photo so that
        eggs were measured blind to treatment information

    -   cg, prev_tray, new_tray - redundant columns used for a different
        experiment.

    -   clutch_code - random number code assigned to photograph to
        measure egg size blind to treatment information

**wild moths hatch dates.csv**

-   contains the ID of all female winter moths caught in Wytham Woods in
    winter 2025, to act as a control group.

-   columns include:

    -   female_ID

    -   capture_date - date removed from trap in Wytham Woods.

**wild moths spreadsheet.csv**

-   contains data on the wild female winter moths caught in Wytham Woods
    in winter 2025, to act as a control group.

-   columns include:

    -   female_ID

    -   capture_date

    -   tree_ID - the identity of the tree in Wytham Wood on which the
        female was caught using a lobster-pot trap

    -   green_eggs - number of green eggs in clutch

    -   orange_eggs - number of orange eggs in clutch

    -   eggs_photographed - used to note whether the clutch had been
        photographed for measuring

    -   egg_area - mean egg size in that clutch, laid by that female. -
        notes

**wild raw egg sizes.csv**

-   contains the measurments of individual eggs measured from the
    photographs taken of the clutches of wild moths

-   columns include:

    -   clutch_code - corresponds to female_ID column in wild moths
        spreadsheet.csv

    -   egg_number - the number of the individual egg measured from that
        photograph

    -   mean area - mean egg size of all eggs measured from the clutch
        photograph. corresponds to egg_area in wild moths
        spreadsheet.csv

**pupation data(Sheet1).csv**

-   pupation date of individuals used in experiment 1

-   columns include:

    -   pupa_id

    -   date

    -   notes

    -   death_date

## Experiment 2

**eggs spreadsheet(Sheet1).csv**

-   contains the measured sizes of the 200 individual moth eggs that
    were reared to caterpillars for experiment 2.

-   columns include:

```         
-   clutchID

-   eggID

-   code_name - the randomised code assigned to the photo, so that
    photos were measured blind to treatment information

-   first photo - a '1' indicates that a first photo was taken

-   size_01 - the measured area of the egg in mm\^2

-    repeatability photo - a '1' indicates that a second photo was
    taken to calculate repeatability of egg size measurements

-   size_02 - the area of the egg measured from the second photo
    (the repeatability photo)
```

**HG_hatch_data(Sheet1).csv**

-   contains the hatch dates of caterpillars reared in experiment two,
    as well as their recorded weights

-   columns include:

    -   hatch_date

    -   eggID

    -   weighday_1 - date of first weighing, 18 days after hatching

    -   weight_1 - weight in mg at weighday_1

    -   weightday_2 - date of second weighing at 24 days after hatching

    -   weight_2 - weight at weightday_2

    -   weightday_3 - date of third weighing at 30 days after hatching

    -   weight3 - weight at weighday_3

    -   weighday_4 - date of fourth weighing at 36 days after hatching

    -   weight4 - weight at weighday_4

    -   weighday_5 - date of fifth weights at 42 days after hatching

    -   weight_5 - weight at weighday_5

    -   weighday_6 - date of sixth weighing at 48 days after hatching

    -   weight_6 - weight at weighday_6

    -   pupation_date
