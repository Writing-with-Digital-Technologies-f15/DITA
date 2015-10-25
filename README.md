# DITA

Repo for student [reusable content projects](http://4662wf15.clindgrencv.com/#reusable-content-projects), writing with DITA.

## Required Tools

1. Text editor (with syntax highlighting)
2. [DITA 1.2 Specifications](http://docs.oasis-open.org/dita/v1.2/spec/DITA1.2-spec.html)
3. [DITA Open Toolkit 2.1.1](http://www.dita-ot.org/2.1/)

## DITA-OT Installation

**Installation tasks**
1. Download and install, (or verify that it is installed), Java JDK (version 7+)
2. Download and install the DITA Open Toolkit (2.1.1)

Before using the DITA-OT, be sure to properly set it up on your computer: [http://www.dita-ot.org/2.1/getting-started/index.html](http://www.dita-ot.org/2.1/getting-started/index.html). You will need JAVA JDK (version 7+) on your computer prior to setting up the ToolKit.

###1. Java Installation

Check to see if Java has been installed on your computer by opening up the terminal, and completing the following steps:

1. Type <code>java --version</code>
2. If the output indicates that you have Java JDK (7+), then continue to task #2: Downloading and installing the DITA OT. If not, go to the [Java download page](http://www.oracle.com/technetwork/java/javase/downloads/jdk7-downloads-1880260.html) and follow the installation instructions for your particular operating system.

###2. Downloading and installing the DITA OT

####OT Installation on Windows

The following steps guide you to set up the DITA Open Toolkit processing environment.

1. Download the DITA Open Toolkit package: [https://github.com/dita-ot/dita-ot/releases/tag/2.1.1](https://github.com/dita-ot/dita-ot/releases/tag/2.1.1).

2. Unzip the package file into the installation directory of your choice. For example <code>C:&#92;pkg&#92;dita-ot-2.1.1</code>

3. Set up DITA_HOME environment variable to point to DITA-OT installation directory: <code>set DITA_HOME=&lt;DITA-OT_dir&gt;</code>

4. Test the DITA-OT installation with the either samples included in the OT, or the basic samples in this repo: <code>DITA/examples</code>.

####OT Installation on Linux or OS X

The following steps guide you to set up the DITA Open Toolkit processing environment in Linux or OS X.

1. Download the DITA Open Toolkit package: [https://github.com/dita-ot/dita-ot/releases/tag/2.1.1](https://github.com/dita-ot/dita-ot/releases/tag/2.1.1).

2. Extract the package file into a installation directory of your choice. For example, your in your home folder: <code>home/dita-ot-2.1.1</code>, or if you are on a Mac, perhaps your Apps folder.

3. Verify that the environment variable JAVA_HOME has been set: <code>export JAVA_HOME=&lt;JRE_dir&gt;</code>

4. Set up DITA_HOME environment variable to point to DITA-OT installation directory: <code>export DITA_HOME=&lt;DITA-OT_dir&gt;</code>

5. To use the <code>dita</code> command anywhere, set up your environment variable: <code>export PATH="${PATH}:/home/lingeringcode/dita-ot-2.1.1/bin"</code>

6. Test the DITA-OT installation with the demo conversions.


## Sample DITA Commands

**Command for <code>dita</code> command help**:

<pre>
username@computername:~/dita-ot-2.1.1$ dita --help
</pre>

**Create an HTML5 site**:

<pre>
username@computername:~/dita-ot-2.1.1$ dita -f html5 -i 'projects/css-projects/understanding_css.ditamap' \
  -o 'projects/css-projects/ex-understanding-css' \
</pre>

**Create an HTML5 site with a custom CSS file**:

<pre>
username@computername:~/dita-ot-2.1.1$ dita -f html5 -i 'projects/css-projects/understanding_css.ditamap' \
  -o 'projects/css-projects/ex-understanding-css' \
  -Dargs.cssroot='projects/css-projects/shared-assets' \
  -Dargs.css='${cssroot}/web-css-grids.css' \
  -Dargs.csspath='css' \
  -Dargs.copycss='yes'
</pre>

