# Population Genomic Analysis 2022 (PGBI11126)

GitHub repository of the [Population Genomic Analysis 2022 (PGBI11126) postgraduate course](http://www.drps.ed.ac.uk/21-22/dpt/cxpgbi11126.htm) at the University of Edinburgh 

Table of contents
-----------------

- [Contacts](https://github.com/LohseLab/PGA_course_2022_DEV/blob/main/README.md#contacts)
- [Course description](https://github.com/LohseLab/PGA_course_2022_DEV/blob/main/README.md#course-description)
- [Course admin](https://github.com/LohseLab/PGA_course_2022_DEV/blob/main/README.md#course-admin)
- [Using this repository](https://github.com/LohseLab/PGA_course_2022_DEV/blob/main/README.md#using-this-repository)
- [Syllabus](https://github.com/LohseLab/PGA_course_2022_DEV/blob/main/README.md#syllabus)

Contacts
--------

- Course organiser: [Dr. Konrad Lohse](mailto:konrad.lohse@ed.ac.uk?subject=[PGA2022])
- Course secretary: [Miss Zofia Bekas](mailto:zofia.bekas@ed.ac.uk?subject=[PGA2022])

Course description
------------------

The course covers the core concepts of modern population genomic analysis which focuses on analysing sequence variation contained in samples of genomes. The aim is to both introduce students to the mathematical models and computational algorithms that describe the ancestry of genomes in evolving populations and show how these are applied in practice to make inferences about the interplay of evolutionary forces (genetic drift, recombination, selection and demographic history) using hands-on data examples. 

The course includes a detailed exposition of the coalescent, the canonical model of sample ancestry and the relevant data structures (genealogies, tree-sequences and graphs) for describing genetic ancestry. A major focus of the course is to understand how this basic stochastic model: 

- extends to include all fundamental evolutionary forces (recombination, population structure, admixture and natural selection) and
- is used to make inferences from both modern and ancient samples using mathematical analysis and simulation.

The course is run as a set of computer practicals which analyse genomic data (both real and simulated) through interactive jupyterLab notebooks. 
Each practical is partnered with a short pre-recorded mini lecture covering the theoretical/conceptual background. 
These should be watched ahead of the corresponding practical session.

Course admin
------------

- PGA consists of a 10 computer practical sesssion (the last one being a class excercise that accounts for 75% of the mark) which analyse population genomic data.
- **The first session will be on Tuesday 18/01 @ 1400-1700 hrs in the [JCMB](https://goo.gl/maps/mYi8YMzKHiA1U9ceA) computer suite Room 1208 (follow the signs to Room 1206C, which is opposite of 1208).**
- Please let [me](mailto:konrad.lohse@ed.ac.uk?subject=[PGA2022]) know beforehand if you have been unable to travel to Edinburgh or are self-isolating, i.e. won't be able to attend.
- While PGA focuses on analysing population genomic data, this will also involve using the Python programming language, which will be introduced gradually throughout the course.
  - if you have not worked with Jupyter notebooks before, please watch [this short intro video](https://www.youtube.com/watch?v=A5YyoCKxEOU) ahead of the course
  - if you are a complete Python-novice, please read sections 1. - 4.3 of the [official Python documentation](https://docs.python.org/3.6/tutorial/)

Using this repository
---------------------
1. Log into [LEARN](https://www.learn.ed.ac.uk/).
2. Go to the [course](https://www.learn.ed.ac.uk/webapps/blackboard/execute/modulepage/view?course_id=_85577_1&cmp_tab_id=_420952_1).  
3. Click on "Course materials", then on the "Notable" icon. <img src="https://user-images.githubusercontent.com/167909/149776450-46ad0b2e-6e64-42b2-87dd-f82875226222.png" width="75%" height="75%">
4. Select the "Chemistry Notebook" from the dropdown menu and click "Start". <img src="https://user-images.githubusercontent.com/167909/149776788-33ba14a5-f22d-4306-82c6-3dbc1e95ff75.png" width="75%" height="75%">
5. Click on `+GitRepo` to bring up the menu to clone this repository. <img src="https://user-images.githubusercontent.com/167909/149777473-e7578276-4f99-44d4-8a68-9ddf06decd43.png" width="75%" height="75%">
6. For this you must enter the following information: <img src="https://user-images.githubusercontent.com/167909/149777230-b3c42388-bd5f-4aaa-96fc-033f90601826.png" width="75%" height="75%">  
  - **Git Repository URL**: `https://github.com/LohseLab/PGA_course_2022`
  - **Branch**: `main` 
7. You can now use the Jupyter file browser to navigate to the notebooks you want to execute.

Syllabus
--------
- `P_01`
  - coalescent simulation and relevant data structures.
  - run and analyse coalescent simulations with `msprime` and `tskit`.
  - understand how the variance of the coalescent depends on the two major axis of sampling: number of loci and number of individuals (Felsenstein 2004).
  - understand why it is natural (and helpful) to treat mutations separately from ancestry.
- `P_02`
  - understand why coalescent simulations are useful to gain intuition about population level processes.
  - appreciate that the site frequency spectrum (SFS) is a fundamental summary of sequence variation and understand how it relates to genealogical branch lengths.
  - understand that summary statistics are the currency for comparing real data to idealized models of population processes/history and that such comparisons can be done either via analytic results or simulations.
  - know how coalescent simulations are used in approximate likelihood inference.
- `P_03`
  - ARGs and treesequences: how are they constructed and how do they differ?
  - appreciate that not all recombination events are detectable
  - understand the difference between map and physical length of a sequence
  - know that the span of trees along the genome is a random variable and that nodes are shared between many trees.
  - understand that the duality between branch lengths and popgen measures extends to correlated trees.
- `P_04`
  - gain familiarity with common bioinformatic file formats (FASTA, BED, VCF)
  - understand how (population) genomic data can be represented through these file formats.
  - know that the analysis of variation data often requires additional simplifications and/or re-classification of the data
  - use common Python libraries to parse, intersect, interrogate, and visualize population genomic data
  - understand that due to background selection, genetic diversity in the genome is strongly correlated with functional constraint
- `P_05`
  - how does positive selection act to favour a beneficial mutation?
  - understand the role of drift/randomness on allele ferquency trajectories and fixation probability
  - understand the effect of positive selection on linked neutral variation
  - understand how `sweepfinder` works using simulation data
  - be able to perform a Selective sweep scan on real data
- `P_06`
  - how to estimate differentiation between populations/species using 𝑑𝑥𝑦, 𝑑𝑛𝑒𝑡 and 𝐹𝑠𝑡 and understand how these summary statistics are defined and related to each other.
  - be able to use coalescent theory to relate estimates of divergence and differentiation obtained from whole genome data to models of equilibrium population structure and non-equilibrium population history.
  - be able to define outliers of differentiation in a genome scan.
  - be able to simulate sequence data under models of population structure and compare these to real data. 
- `P_07`
  - appreciate the infromation about the divergence history of populations contained in incomplete lineage sorting  
  - learn how to detect introgression from archaic Hominins into modern humans using the D statsitic (aka the ABBA/BABA test)
  - TBA
- `P_08` - `P_09`
  - Applying the knowledge you gained from this course to novel, real-world datasets.
  - TBA
  
