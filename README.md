### Who is covered on the news?

We merge the [Stanford Cable TV News Analyzer Data](https://tvnews.stanford.edu/) with the [Voteview Data](https://voteview.com/) and [DIME data](https://data.stanford.edu/dime) to estimate the extremity of the politicians covered on cable news.


We have four hypotheses:

1. We hypothesize a sharp skew in the coverage with the president and a few other prominent national politicians hogging most of the coverage
2. We hypothesize that executives are covered more than the legislative or the judicial branch
3. We hypothesize that extreme politicians are covered more than moderate politicians.
4. We hypothesize that partisan channels cover extreme members of the other party more often than their own party.

### Assumptions

When merging the data, we take the most recent ideology scores even though the politician data is spread over multiple years.

### Scripts

* [Merge archive.org with voteview and DIME data](scripts/merge.R)
* [Figure 1: Dotplot of top 50 politicians](scripts/fig1_top50.R)
* [Figure 2: Dotplot of executive coverage vs. rest](scripts/fig2_executive_rest.R)
* [Figure 3a: Density plot of ideology weighted by coverage using Voteview](scripts/fig3_density_plot_voteview.R)
* [Figure 3b: Density plot of ideology weighted by coverage using DIME](scripts/fig3_density_plot_dime.R)
* [Figure 4a: Density plot of ideology weighted by coverage using Voteview by Channel](scripts/fig4_density_plot_voteview_channel.R)
* [Figure 4b: Density plot of ideology weighted by coverage using DIME by Channel](scripts/fig4_density_plot_dime_channel.R)

### Authors

Lucas Shen Yan Shun and Gaurav Sood
