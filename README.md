# git-chart

`git-chart` is a simple Perl script that generates a plot of commits over time
for a given repository. This was created as a quick&dirty hack, so expect rough
edges and lots of missing features.

Also note that it was developed independently and bears no relation to [flashcode's
gitchar](https://github.com/flashcode/gitchart) program, despite the similarity
in name and intent.

# Usage

	Usage: git chart [options...] [log specs...]

	Creates a chart plotting the distribution over time of the commits
	specified as <log specs>. By default, commits are grouped by hour, day,
	week, month or year depending on the time spanned, but this can be
	controlled by the user.

	Options:
		--hourly, --daily, --weekly, --monthly, --yearly:
			force a specific commit grouping
		--step=<integer>:
			force commits to be grouped each <integer> seconds
		--gnuplot:
			produce a chart with gnuplot (default)
		--google:
			produce a chart with Google Charts
		--chart-height=<integer>:
			set the Google Charts height; the width is set
			to a 4:3 ratio (default: 100)

