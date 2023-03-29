# **HTR Sorter**
## **What is this?**
This is a simple code snippet that can sort your HTR results raws into CSV & export them into plots. Since there are many cage types in the raw files, it is important to sort them well. In that situation, this code can help you to sort them easily.

## **About HTR Algorithm**
[HTR Algorithm](https://www.degruyter.com/document/doi/10.1515/ntrev-2022-0044/html) is a ultra-fast tool to identify the cage types in the molecular dynamics (MD) simulations. It is a very useful tool to analyze the cage types in the MD simulations. I highly appreciate the authors of the HTR Algorithm for generously sharing the HTR codes. <br/>

## **Gallery**
| **(1) Number of cage types in each frame** | **(2) The number of dissociated cages** | **(3) Degree of crystallinity** |
| ----- | ----- | ----- |
| <img src = "https://github.com/wjgoarxiv/HTR_sorter/blob/20b69286d4c299d4e7e12faae0f677c463909a8f/Number_of_cage_types.png" style="width: 600px; height:auto;"> | <img src = "https://github.com/wjgoarxiv/HTR_sorter/blob/20b69286d4c299d4e7e12faae0f677c463909a8f/Absolute_changes_from_initial_number_of_cage_types.png" style="width: 600px; height:auto;"> | <img src = "https://github.com/wjgoarxiv/HTR_sorter/blob/20b69286d4c299d4e7e12faae0f677c463909a8f/Degree_of_crystallinity.png" style="width: 600px; height:auto;"> |

## **How to use?**
First, all the code snippets are written in `.ipynb` file format. If you want to see the codes in `.ipynb` file well, go to the following link. <br/>
[HTR_sorter dev link](https://github.dev/wjgoarxiv/HTR_sorter)
<br/>
And then, click `HTR_sorter_notebook.ipynb`. You can see the code snippets and sample outputs in the notebook. 

If you want to download the demo raw files and the source `.ipynb` code, then please type this into your terminal.
```
git clone https://github.com/wjgoarxiv/HTR_sorter.git
```
Then, you can see the `HTR_sorter` folder in your current working directory. <br/>

## **How can we distinguish the identified cage types in raw text files?**
It is easy to identify cage types from the raw text files. For instance, if the following results were represented in the text file:
```
0-12-0:166
0-12-2:479
1-10-4:2
```
Then, we can see that 166 $5^{12}$ cages, 479 $5^{12}6^{2}$ cages, and 2 $4^{1}5^{10}6^{4}$ cages were identified in that frame.

## **How the polished CSV file looks like?**
The polished CSV file looks like the following:
```
Time Step (ns),0-12-0:,0-12-2:,0-12-3:,0-12-4:,0-12-5:,0-12-6:,0-12-8:,1-10-2:,1-10-3:,1-10-4:,2-8-1:,2-8-2:,2-8-3:,3-6-3:
0,166,479,0,0,0,0,0,6,1,2,2,0,1,0
1,180,504,1,0,0,0,0,4,5,1,0,2,4,0
2,178,515,1,0,0,0,0,6,3,1,1,0,1,0
3,186,521,2,0,0,0,0,5,1,1,0,4,1,1
4,183,521,1,0,0,0,0,8,1,1,1,1,3,0
...
```
You can see the details in the `output.csv` file in the `HTR_sorter` folder.

## **Functionalities**
- [x] Sort the raw text files into CSV files
- [x] Export the CSV files into plots
- [x] User can select the cage types to be plotted (with the ipywidgets)
- [x] Degree of crystallinity of sI (or sII) can be plotted
