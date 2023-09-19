# conda虚拟环境

<hr>


Conda的虚拟环境是一种可以让开发者在同一台计算机上创建和管理多个相互独立的Python环境的工具。每个虚拟环境可以具有自己的Python解释器和包集合，这意味着开发者可以在不同的虚拟环境中安装和管理不同版本的Python包，而不会相互干扰。

以下是使用Conda创建和管理虚拟环境的步骤：

## 安装Conda

首先，开发者需要安装Conda。开发者可以从官方网站下载并安装Conda，或者使用Anaconda或Miniconda安装包。安装后，开发者需要在终端或命令提示符中运行以下命令以确保Conda已成功安装：

```
conda --version
```


<hr>


## 创建虚拟环境

要创建虚拟环境，请打开终端或命令提示符，并输入以下命令：

```
conda create --name <environment-name> <package-name>
```
其中，<environment-name>是虚拟环境的名称，<package-name>是要在该环境中安装的包的名称。如果开发者不指定<package-name>，则会创建一个新的虚拟环境，其中只有基本的Python包。

例如，要创建一个名为 **MyEnv** 的虚拟环境，并在其中安装Python 3.7和numpy包，请运行以下命令：

```
conda create --name MyEnv python=3.7 numpy
```

<hr>

## 激活虚拟环境

创建虚拟环境后，开发者需要激活它以使用其中的Python解释器和包。要激活虚拟环境，请在终端或命令提示符中运行以下命令：

```
conda activate EnvironmentName
```
其中， EnvironmentName 是开发者想要激活的虚拟环境的名称。

例如，要激活名为**MyEnv**的虚拟环境，请运行以下命令：
```
conda activate MyEnv
```

<hr>

## 在虚拟环境中安装包

要在虚拟环境中安装包，请激活虚拟环境并使用conda install命令安装包。例如，要在名为**MyEnv**的虚拟环境中安装pandas和matplotlib包，请运行以下命令：
```
conda activate MyEnv
conda install pandas matplotlib
```

<hr>

## 退出虚拟环境

要退出当前虚拟环境，请在终端或命令提示符中运行以下命令：
```
conda deactivate
```

<hr>

## 删除虚拟环境

如果开发者不再需要某个虚拟环境，可以使用以下命令将其删除：

```
conda remove --name EnvironmentName --all
```

<hr>

## 问答环节

### 问答1

**Q:如何查看conda虚拟环境列表以显示所有的虚拟环境？**

A:要查看conda虚拟环境列表并显示所有的虚拟环境，请在终端或命令提示符中运行以下命令：

```
conda info --envs
```
该命令将显示所有当前可用的conda虚拟环境，其中星号（*）表示当前激活的虚拟环境。

<hr>

### 问答2

**Q:在conda虚拟环境中可以使用pip命令吗?**

A:是的，在conda虚拟环境中也可以使用pip命令来安装和管理Python包。

虽然Conda是一个非常强大的Python包管理工具，但有些包可能无法在Conda存储库中找到。在这种情况下，开发者可以使用pip命令在conda虚拟环境中安装这些包。

要在conda虚拟环境中使用pip命令，请先激活虚拟环境，然后使用pip install命令来安装包。例如，要在名为myenv的虚拟环境中使用pip安装requests包，请运行以下命令：
```
conda activate myenv
pip install requests
```
需要注意的是，在conda虚拟环境中使用pip命令可能会与conda包管理器产生冲突。因此，建议在conda虚拟环境中只使用pip安装Conda无法提供的包，而使用conda安装大多数其他Python包。

<hr>

### 问答3

**Q:在conda虚拟环境中，使用pip安装的python包是不是安装在虚拟环境中？**

A:是的，在conda虚拟环境中使用pip安装Python包将安装在该虚拟环境中，而不是全局Python环境中。这意味着虚拟环境中安装的包仅对该虚拟环境中的Python解释器可用，并且不会影响全局Python环境或其他虚拟环境。

当开发者使用conda create命令创建新的虚拟环境时，Conda会自动安装一个新的Python解释器和必要的依赖项。然后，当开发者在虚拟环境中使用pip install命令来安装包时，它们将被安装在该虚拟环境的Python解释器下的site-packages目录中，而不是全局Python解释器下的site-packages目录中。

这种方式可以避免因安装包而导致的版本冲突问题，并允许开发者在不同的项目中使用不同的包版本。



<hr>

### 问答4

**Q:如果我之前已经用pip安装了numpy，启动conda的虚拟环境后，如果用命令行运行一个脚本case.py，case.py中会引入numpy，那么case.py中引入的numpy是虚拟环境中的numpy，还是之前用pip安装好的numpy？**

A:在使用conda和pip管理Python包时，可能会遇到多个Python环境和包版本的问题。为了解决这些问题，可以使用conda的虚拟环境来隔离项目所需的Python环境和包。假设在此前提下，已经使用pip在系统级别上安装了numpy包。

在启动conda虚拟环境后，所有的命令和脚本都将使用该环境中的Python解释器和包。因此，在运行case.py脚本时，该脚本将使用虚拟环境中的Python解释器和包。如果在虚拟环境中没有安装numpy，则引入numpy的代码将会出现错误。因此，如果需要在虚拟环境中使用numpy，需要在该环境中使用conda或pip安装它。

如果已经在虚拟环境中安装了numpy，则case.py将使用该虚拟环境中的numpy包。这是因为在虚拟环境中，每个环境都有自己的包集合，不同虚拟环境中的包是相互独立的。因此，即使在系统级别上使用pip安装了numpy包，也不能在虚拟环境中使用它，除非在虚拟环境中使用pip或conda安装numpy包。