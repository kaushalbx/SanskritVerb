# SanskritVerb

Verb declension for Sanskrit

**As of *v1.2.0*, the code from [`drdhaval2785/SanskritSubanta`](https://github.com/drdhaval2785/SanskritSubanta) for *subanta* generation is now actively maintained here.**

## Code Structure
To understand how the code is organized, please read [this](https://github.com/drdhaval2785/SanskritVerb/blob/master/Documentations/understandcode.md).

A research paper on the *subanta* generator which was presented at 16th World Sanskrit Conference can be found [here](http://www.sanskritworld.in/index/detailview/book_id/prakriyapradarshini).

## Online Demo

* Use http://www.sanskritworld.in/sanskrittool/SanskritVerb/tiGanta.html for *tiGanta* generation (verb conjugation)
* Use http://www.sanskritworld.in/sanskrittool/subanta.html for *subanta* generation
* Use http://www.sanskritworld.in/sanskrittool/sandhi.html for *sandhi* generation.

## Running the Code Locally with Docker

1. Install [Docker](https://www.docker.com/) (can be done through Homebrew)
2. Clone this repo and `cd` into it
3. `docker build -t sanskrit-verb .`
4. `docker run -p 3333:80 sanskrit-verb`
5. Go to `localhost:3333/SanskritVerb`

## Running the Code with XAMPP

This is a one time exercise. Once you have completed the steps below, you should only open your browser (Firefox, Chrome, Internet Explorer, etc.) and browse to `localhost/SanskritVerb/tiGanta.html` to access a frontend that will allow you to interact with the machine.

1. Download the latest version of XAMPP from https://www.apachefriends.org/index.html
2. Install XAMPP.
3. Install Git from https://git-scm.com/downloads.
4. Locate XAMPP directory. Usually it is `c://xampp`.
5. Right-click on `xampp-control.exe` and select 'Run As Administrator'. (For steps 5-8, if in doubt, please see [this](http://stackoverflow.com/questions/20960296/how-to-start-apache-and-mysql-automatically-when-windows-8-comes-up))
6. In the right-top corner, click on '**Config**'.
7. Tick **Apache**, **FileZilla**, **Tomcat**, **MySQL** and **Mercury** in '**Autostart of modules**' section.
8. Click '**Save**'.
9. Close '**XAMPP Control Panel**'.
10. go to `xampp/htdocs` directory.
11. Copy [`install.sh`](https://github.com/drdhaval2785/SanskritVerb/blob/master/install.sh) in that directory.
12. Click on `install.sh`. This will fetch the latest code and data for local usage.

## Changelog

#### **v1.0.0** (2 August 2015)
* Initial release

#### **v1.0.1** (5 October 2015)
* Major bug fixes

#### **v1.1.0** (17 October 2015)
* Time optimization

#### **v1.1.1** (26 October 2015)
* Noted all inline issues from `tiGanta.php` and `function.php` as Github issues for easier tracking

#### **v1.1.2** (7 November 2015)
* Separated code into `Data`, `Documentations`, `scripts`, `testing` and `output` folders
* Made necessary corrections to the code

#### **v1.2.0** (12 January 2016)
* Merged **SanskritSubanta** code into **SanskritVerb**
* There is now only one file `panini.php` which gives *subanta* / *tiGanta* / *sandhi* etc depending on the input HTML file

#### **v1.3.0** (22 January 2016)
* Added commentaries available for local viewing

#### **v1.4.0** (3 February 2016)
* Added the option to deactivate some *sUtras* of Paninian grammar (to understand its importance in the structure of **aSTAdhyAyI**)

#### **v1.5.0** (21 February 2016)
* Tested the code for representative verbs and corrected suspect verb forms

#### **v1.6.0** (21 February 2016)
* Made three commentaries available for offline viewing:
    * **mAdhavIyadhAtuvRtti**
    * **kSIrataraGgiNI**
    * **dhAtupradIpa**

#### **v1.6.1** (12 March 2016)
* Tested the code for representative verbs from **siddhAntakaumudI** (round 2) and corrected suspect verb forms

#### **v1.7.0** (13 March 2016)
* Defined which *sUtra* bars which *sUtras*

#### **v1.8.0** (20 March 2016)
* Added the following forms:
    * **bhAvavAcya**
    * **karmavAcya**
    * **karmakartRvAcya**
    * **Nijanta**
    * **yaGanta**

#### **v1.9.0** (26 March 2016)
* Added the following forms:
    * **yaGluganta**
    * **sannanta**

#### **v1.10.0** (19 June 2016)
* Tested the output against [UoHyd](http://sanskrit.uohyd.ac.in/scl/) and [INRIA](http://sanskrit.inria.fr/DATA/XML/SL_morph.tar.gz) databases and accounted for all differences

#### **v1.10.1** (06 September 2016)
* Readjusted the `sandhi.html` and `subanta.html` frontends with `panini.php` (After changes for optimization in *tiGanta* generation, it stopped working)
