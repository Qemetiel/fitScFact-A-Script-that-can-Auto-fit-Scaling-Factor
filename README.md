# fitScFact-A-Script-that-can-Auto-fit-Scaling-Factor
A shell script to auto-calculate quantum chemistry scaling factors for ZPE &amp; frequencies. No more retrieval database &amp; manual fitting! Supports custom datasets. Just run ./fitScFact.sh "method/basis".

# Auto-fit-Scaling-Factor

A shell script to automatically calculate the Zero-Point Energy (ZPE) scaling factor for quantum chemical calculations.

## Overview

This script automates the process of fitting scaling factors for vibrational frequencies and zero-point energies (ZPE), as detailed in the popular computational chemistry blog post by Sobereva (["自行拟合基频校正因子与ZPE校正因子的简单方法"](http://sobereva.com/585)).

It is designed for researchers who use quantum chemistry methods (e.g., DFT functionals like B3LYP) for which pre-tabulated scaling factors may not be available. By automating the fitting process, it saves significant time and effort compared to manual fitting.

## Key Features

*   **Automatic Fitting**: Automatically computes the ZPE scaling factor for any given theoretical method (e.g., `"b3lyp/6-31g*"`).
*   **Pre-defined Datasets**: Includes the `ZPVE15/10` dataset from JCTC, 6, 2872 (2010) by Truhlar et al. for immediate use.
*   **Custom Datasets**: Supports user-defined training sets by simply adding Gaussian input (`.gjf`) files in a specified directory structure.
*   **Gaussian Integration**: Seamlessly works with Gaussian 16, leveraging its output for frequency calculations.
*   **Comprehensive Output**: Provides the fitted scaling factor and generates a `ZPE.txt` file for result verification.

## Usage
See:  http://bbs.keinsci.com/forum.php?mod=viewthread&tid=53003&fromuid=36454
1.  Ensure Gaussian 16 is installed and properly configured in your environment.
2.  Run the script from your terminal, specifying the method and basis set:

## Example
Change "trainingSet" in fitScFact.sh to Z1 Data Set 
Run: ./fitScFact.sh "b3lyp 6-31g*"
Print: sc1ZPE=0.980794

# Auto-fit-Scaling-Factor (自动拟合校正因子)

一个用于自动计算量子化学计算中零点能（ZPE）校正因子的 Shell 脚本。

## 项目简介

本脚本自动化了振动频率和零点能（ZPE）校正因子的拟合过程。该过程基于思想家公社的 Sobela 博主在其博文《[自行拟合基频校正因子与ZPE校正因子的简单方法](http://sobereva.com/585)》中详细介绍的方法。

对于使用某些量子化学方法（如特定的 DFT 泛函和基组）的研究者来说，可能找不到现成的校正因子。本脚本通过自动化整个拟合流程，极大地节省了手动拟合所需的时间和精力。

## 主要功能

*   **自动拟合**: 为任何给定的理论计算方法（例如 `"b3lyp/6-31g*"`）自动计算 ZPE 校正因子。
*   **内置数据集**: 内置了 Truhlar 等人文章 (JCTC, 6, 2872 (2010)) 中的 `ZPVE15/10` 数据集，开箱即用。
*   **自定义数据集**: 支持用户自定义训练集，只需按照规定的目录结构添加 Gaussian 输入文件 (`.gjf`) 即可。
*   **Gaussian 集成**: 与 Gaussian 16 协同工作，直接调用其进行频率计算并处理输出结果。
*   **完整输出**: 提供拟合出的校正因子，并生成 `ZPE.txt` 文件供用户查看和验证详细结果。

## 使用方法
可见：一键拟合任意级别ZPE校正因子的小脚本fitScFact (http://bbs.keinsci.com/forum.php?mod=viewthread&tid=53003&fromuid=36454)
1.  确保 Gaussian 16 已安装且环境变量配置正确。
2.  在终端中运行脚本，并指定计算方法和基组：
