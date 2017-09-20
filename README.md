# Learning cluster computing on Sango and snakemake

Note: before you begin the exercise, make sure you add `/apps/unit/MikheyevU/sasha/miniconda3/bin` to your PATH.

The objective is to create a tab-delimited database of countries, capitals and currencies, like that in `data/countries, capitals and currencies.txt`. To do this, you have two pairs of files, one pair containig countries and currencies, and another pair containing countries and capitals.

I suggest getting the script working on the head node first, without using sbatch, and doing the job submission as part of the last step.

1. Clone the repository 
2. Make a branch with your own name, and switch to that branch
3. Write a snakemake rule that processes each pair of files country/capital and country/currency files and creates a pair of tab-delimited country/capital/currency files. This rule should act on each pair separately, i.e., using two separate tasks that can, in principle be run in parallel.
4. Write a rule that combines the output of the previous rule into a tab-delimited database coutaining all the data.
5. Write a rule verifying that the information content in your output corresponds to that of the reference database in `data/countries, capitals and currencies.txt`
6. Run the jobs on sango, add sango logs to the repository, commit them to the repo and push the results to github.
