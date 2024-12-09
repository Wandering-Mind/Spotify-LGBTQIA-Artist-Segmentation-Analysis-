Hi Everyone,
The main concern my analysis seeks to assess is the general relationships between LGBTQIA artists registered on Spotify's Platform who appear in our list of Most Streamed Spotify Songs (including the creator(s)). Here are the links to some of the websites I used to scrape the data:
(a) GLOW - Spotify's Equity Program for LGBTQIA+ Artists 
(b) Happy pride! In honor of the month, here is a list of 100+ LGBT artists to listen to and support 🏳️‍🌈 : r/popheads
(c) Over 100 LGBTQ+ Artists You Should Check Out! : r/indieheads
PART 1: Variable Addition 
Here’s what I did:
(a)	Create a new sheet in the existing excel workbook – call it “LGBTQIA Count Data” 
(b)	Within “LGBTQIA Count Data” sheet insert the following:
a.	Column A = title “Queer Artists” (compiled manually from sources above) // Column B = “General Artist List” (list of artists from column C in the main dataframe in “Most Streamed Spotify Songs 2024”)
(c)	Standardize the data (inside “LGBTQIA Count Data):
a.	Column C = title “Edited Queers” // Column D = title “Edited General Artists” 
b.	Insert this formula into column C2 and drag down/cluck bottom right corner to apply for whole column:

=UPPER(TRIM(A2))

c.	Insert this formula into column D2 and drag down/click bottom right corner to apply for whole column:

=UPPER(TRIM(B2))

(d)	Apply LGBTQIA+ formula in column E, titled “LGBTQIA+” (within the “LGBTQIA Count Data sheet):
a.	Insert this formula into column E2 and drag down/cluck bottom right corner to apply for whole column:

=IF(COUNTIF($C$2:$C$470, D2) > 0, 1, 0)

b.	This formula returns a value of ‘1’ if the artist appears on the “Queer Artists” list, and 0 if the name/title does not
(e)	Copy only the values in column E and paste them in to column AD (titled “LGBTQIA+”) . Make sure the formula is not pasted, only the values themselves.

PART 2: Popularity  Variable Analysis 
Popularity Scoring Pivot Table (title: PopularityScoringPT)
The goal for this analysis was to find the average Spotify popularity score of LGBTQIA+ artists vs non-LGBTQIA+ artists. My findings are below:
(a)	The average Spotify popularity of LGBTQIA+ individuals is 3.954234171 higher than non-LGBTQIA identifying artists, meaning that LGBTQIA+ artists have a higher popularity score than non-LGBTQIA+ artists in 2024. 

Part 3: 
Social Media Likability Pivot Table (title: YT_TT_SHZ_EXP)
YT (YouTube), TT (Tik Tok), SHZ (Shazam), EXP (Explicit Track) variables are all pulled from the “MostStreamedSpotifySongs2024” and stratified using the system of ‘0’ as non-identifying as LGBTQIA and ‘1’ as identifying as LGBTQIA. The insight(s) derived yield an increasing number of LGBTQIA artists art are interacted with more than ever before. In addition, there is data that shows 5% of all artists listed who identify as LGBTQIA produce explicit tracks, 8% of thee same artists are shazam’d, 8% share the likecounts on Tik Tok and 7% share the total like amount on YouTube





