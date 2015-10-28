# DITA

Repo for student [reusable content projects](http://4662wf15.clindgrencv.com/#reusable-content-projects), writing with DITA.

## Required Tools

1. Text editor (with syntax highlighting)
2. [Java JDK 7+](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
3. [DITA 1.2 Specifications](http://docs.oasis-open.org/dita/v1.2/spec/DITA1.2-spec.html)
4. [DITA Open Toolkit 2.1.1](http://www.dita-ot.org/2.1/)

## DITA-OT Installation

**Installation tasks**

1. Read up on terminal / shell use, if you are not familiar with using the command-line interface.
2. Verify if Java JDK (version 7+) is installed by running <code>java -version</code> in your terminal / shell. **If installed**, go to task #3. **If not installed**, go to task #2.
3. Download and install the DITA Open Toolkit (2.1.1)

Before using the DITA-OT, be sure to properly set it up on your computer: [http://www.dita-ot.org/2.1/getting-started/index.html](http://www.dita-ot.org/2.1/getting-started/index.html). You will need JAVA JDK (version 7+) on your computer prior to setting up the ToolKit.

###1. Terminal / Shell Use

Linux and Mac OS use the Terminal command-line interface, while Windows uses the shell command-line interface. As noted on the DITA-OT site, the toolkit is a command-line tool with no GUI. If you are unfamiliar with how to use the terminal (Linux / Mac OS) or shell (Windows), here is how to locate and open it on your computer.

**Mac OS**: On Mac, look under Utilities and open the "Terminal." Read this [introduction to the terminal](http://blog.teamtreehouse.com/introduction-to-the-mac-os-x-command-line) blog post to learn some basic terminal commands.

**Windows**: On Windows, search for the cmd.exe file or "Command Prompt" and create a shortcut to it within a directory of your choice (e.g., Desktop). Read this [introduction to the Windows shell](http://www.computerhope.com/issues/chusedos.htm) to learn some basic commands.

###2. Java Installation

Check to see if Java has been installed on your computer by opening up the terminal / shell, and completing the following steps:

1. Type <code>java -version</code>
2. If the output indicates that you have Java JDK (7+), then continue to task #3: Downloading and installing the DITA OT. If not, go to the [Java download page](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) and follow the installation instructions for your particular operating system: [Windows](https://docs.oracle.com/javase/8/docs/technotes/guides/install/windows_jdk_install.html#CHDEBCCJ), [Mac OS X](https://docs.oracle.com/javase/8/docs/technotes/guides/install/mac_jdk.html#CHDBADCG), [Linux](https://docs.oracle.com/javase/8/docs/technotes/guides/install/linux_jdk.html#BJFGGEFG)
3. After installing Java, set the PATH environment variable. For Windows, see the [Java documentation](https://docs.oracle.com/javase/8/docs/technotes/guides/install/windows_jdk_install.html#BABGDJFH)

###3. Downloading and installing the DITA OT

####OT Installation on Windows

The following steps guide you to set up the DITA Open Toolkit processing environment.

1. Download the DITA Open Toolkit package: [https://github.com/dita-ot/dita-ot/releases/tag/2.1.1](https://github.com/dita-ot/dita-ot/releases/tag/2.1.1).

2. Unzip the package file into the installation directory of your choice. For example <code>C:&#92;pkg&#92;dita-ot-2.1.1</code>

3. To use the <code>dita</code> command anywhere, set up your environment variable by following this [tutorial](http://4662wf15.clindgrencv.com/cmdline.html#windows-path-envar).

4. Test the DITA-OT installation with the either samples included in the OT, or the basic topic models in this repo: <code>DITA/examples</code>.

####OT Installation on Linux or OS X

The following steps guide you to set up the DITA Open Toolkit processing environment in Linux or OS X.

1. Download the DITA Open Toolkit package: [https://github.com/dita-ot/dita-ot/releases/tag/2.1.1](https://github.com/dita-ot/dita-ot/releases/tag/2.1.1).

2. Extract the package file into a installation directory of your choice. For example, your in your home folder: <code>home/dita-ot-2.1.1</code>, or if you are on a Mac, perhaps your Apps folder.

3. To use the <code>dita</code> command anywhere, set up your environment variable by following this [tutorial](http://4662wf15.clindgrencv.com/cmdline.html#mac-path-envar).

4. Test the DITA-OT installation with the either samples included in the OT, or the basic topic models in this repo: <code>DITA/examples</code>.


## Building DITA Transformations

See the DITA-OT user guide about how to generate output: [http://www.dita-ot.org/2.1/getting-started/using-dita-command.html](http://www.dita-ot.org/2.1/getting-started/using-dita-command.html)

### Sample DITA Commands

**See the <code>dita</code> command help**:

<pre>
username@computername:~/dita-ot-2.1.1$ dita --help
</pre>

<pre>
/* DITA options and arguments */

-f == dita output format
-i == dita input map file
-o == dita output directory
-D&lt;property&gt;=&lt;value&gt; == add custom args 
    with particular values to dita transformation
-filter &lt;file&gt; == filter and flagging file (e.g., .ditaval)
</pre>

**Create a PDF**:

<pre>
username@computername:~/dita-ot-2.1.1$ dita -f pdf -i 'projects/css-projects/understanding_css.ditamap' \
  -o 'projects/css-projects/out/pdf/ex-understanding-css'
</pre>

**Create an HTML5 site**:

<pre>
username@computername:~/dita-ot-2.1.1$ dita -f html5 -i 'projects/css-projects/understanding_css.ditamap' \
  -o 'projects/css-projects/out/html5/ex-understanding-css'
</pre>

**Create an HTML5 site with a custom CSS file**:

<pre>
username@computername:~/dita-ot-2.1.1$ dita -f html5 -i 'projects/css-projects/understanding_css.ditamap' \
  -o 'projects/css-projects/out/html5/ex-understanding-css' \
  -Dargs.cssroot='projects/css-projects/shared-assets' \
  -Dargs.css='${cssroot}/web-css-grids.css' \
  -Dargs.csspath='css' \
  -Dargs.copycss='yes'
</pre>
