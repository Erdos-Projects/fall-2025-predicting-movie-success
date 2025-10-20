# fall-2025-predicting-movie-success
Team project: fall-2025-predicting-movie-success

## Project Defintion: 
Question we are asking: Can large scale aggregates of review data predict critical movie success? 

## Statistical Strategy
1. Our goal will be to score individual reviewers based on how well they can predict critical movie success, in particular relative to a set of predetermined prestigious movie awards.
2. Every reviewer will have an individual review distribution $f(user)$ consisting of their own reviews written for every movie while every movie will have a similar distribution $f(movie)$ consisting of every review for that movie.
3. Fit all distibutions $f(user)$ and $f(movie)$ to normals to obtain the mean $\mu(user), \mu(movie)$ and standard deviation $\sigma(user),\sigma(movie)$. 
4. Any given review $x_{user,movie}$ written by user will have two $z$-scores, relative to both $f(user)$ and $f(movie)$. Assign the joint significance as $z_{joint}=z_{user}*z_{movie}$. 
5. For a benchmark dataset of previous award winning and nominated movies (we can have a few different data sets here, one for only winners, one for all nominated, etc), create a new distribution $f_{score}(user)of all $z_{joint}$ values.
6. Rank users by highest average $\mu(joint)$ of their $f_{score}$ distribution.
7. Form an aggregate of the highest $n$ rated users on letterboxd as "the most discerning users" and attempt to see if they have preditive power for awards via back testing. 

## Tasks to do

~1. Build Movie histogram scraping script~ Done

2. Build Individual reviewer histogram and detailed scraping script

3. Build web navigating script, going from reviewer to reviewer, movie to movie etc.

4. Collect data on awards and timings

5. Build Data aggregating script

6. Analyze data

