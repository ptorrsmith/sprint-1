Command line adavnced

Standard input and Standard output

stdin - input to terminal by keyboard or input device

stdout - information/result output by terminal 

stderr - output error from a failed command

uniq file.txt = Shows file contents of file.txt excluding duplicates that are sequential

Best to sort then uniq, e.g. 
sort file.txt | uniq > sorted-file.txt

grep = global regular expression print

grep searches filesnames, foldernames, and file contents for matching patterns

e.g. grep SearchTerm file.txt - looks for the exact case matching term "SearchTerm".  grep -i makes the search case insenstive.

grep -R = recursive


sed - stream editor
sed 'expression' file.txt - takes file.txt as input, and outputs modified results through an expression

e.g. sed 's/abc/xyz' file.txt - outputs file contents substituting abc text with xyz. Note: this will only substitute the first instance found of the pattern text abc in file.txt


echo $HOME - home directory variable value

echo $PATH - list of directories separated by a :

env - returns all environment variables
env | grep PATH - returns lines with the text PATH


