# 发票数据提取工具

本 Python 脚本旨在分析 PDF 发票并提取相关信息，然后将其整理并保存在 Excel 电子表格中用于报销统计。

`Fapiao2Excel.py`

## 先决条件

在运行脚本之前，请确保已安装以下依赖项：

- Python（3.x）
- pandas
- [pdfplumber](https://github.com/jsvine/pdfplumber)
- [openpyxl](https://openpyxl.readthedocs.io/)
- 根据您的具体 PDF 发票格式需要的其他依赖项

您可以使用 pip 安装所需的 Python 包：

```bash
pip install pdfplumber pandas openpyxl
```

## 用法

要使用此工具，请按照以下步骤操作：

使用以下命令运行脚本：

   ```bash
   python 脚本名称.py --path 输入PDF目录 --output 输出Excel文件.xlsx
   ```

   将“脚本名称.py”替换为脚本的实际名称。

   - `--path`（或 `-p`）：这是一个必需参数，应该是包含您的 PDF 发票的目录路径。
   - `--output`（或 `-o`）：这是一个可选参数，用于指定输出的 Excel 文件。如果未提供，默认文件名为“result.xlsx”。

## 输出

脚本将处理指定目录中找到的 PDF 发票，提取相关数据，并将其保存在一个名为“发票”的 Excel 电子表格中。

为了最简单的使用，输出只包含下面5列信息：


| id | 发票号码	| 开票日期	| 价税合计(大写)	| 价税合计(小写) |
| --- | --- | --- | --- | --- |

## 示例运行

```bash
python invoice_extraction.py --path /path/to/pdf_invoices --output my_invoices.xlsx
```


## 鸣谢

- [Invoice2Excel](https://github.com/yooongchun/Invoice2Excel)
- [pdfplumber](https://github.com/jsvine/pdfplumber)
- [openpyxl](https://openpyxl.readthedocs.io/)

