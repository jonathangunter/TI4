TI4 Statistics
================
Jonathan Gunter
9/12/2020

## Intro

Jon is learning how to host R analyses on the internet by goofing around
with TI4 data
(<https://docs.google.com/spreadsheets/d/1c2fGqedk13kS8PR2XF1Olo7kWrjUu5LwZFLSRUKaKdo>).

### Which races are played the most?

Unsurprisingly, 5 of the 6 races recommended in the ‘Learn to Play’ game
are the most played. Sardakk, despite being in the Learn to Play game,
is the 3rd least played race. People play them once and then never
again.

![](TI4-Markdown-testing_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->

### Who wins the most?

The Federation of Sol has the most plays along with the most wins. Would
You Like To Know More?

![](TI4-Markdown-testing_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

### Relationship between Plays and Wins

Logically, the more times a race is played, the more wins it should
have. Fitting it to a linear model, we can see that every time a race is
played, we expect it’s win total to increase by \~0.27.

![](TI4-Markdown-testing_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

    ## 
    ## Call:
    ## lm(formula = stats$wins ~ stats$plays)
    ## 
    ## Residuals:
    ##    Min     1Q Median     3Q    Max 
    ## -82.17 -47.51 -27.88  62.09  86.40 
    ## 
    ## Coefficients:
    ##              Estimate Std. Error t value Pr(>|t|)    
    ## (Intercept) -76.50634   54.80728  -1.396    0.183    
    ## stats$plays   0.27215    0.03891   6.995 4.32e-06 ***
    ## ---
    ## Signif. codes:  0 '***' 0.001 '**' 0.01 '*' 0.05 '.' 0.1 ' ' 1
    ## 
    ## Residual standard error: 58.84 on 15 degrees of freedom
    ## Multiple R-squared:  0.7654, Adjusted R-squared:  0.7497 
    ## F-statistic: 48.93 on 1 and 15 DF,  p-value: 4.316e-06

### Outcomes

There is more to the game than winning. Let’s take a look at the final
outcome of all 10 point games played by the Federation of Sol:
![](TI4-Markdown-testing_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max. 
    ##   0.000   6.000   8.000   7.616  10.000  10.000

Even when they don’t win, Sol get a lot of points.

Let’s see the distribution of end game scoring outcomes in 10 point
games for all races:

![](TI4-Markdown-testing_files/figure-gfm/unnamed-chunk-6-1.png)<!-- -->

Let’s see the distribution of outcomes for all races in 14 point games:

### Neat. How about 14 point games?

![](TI4-Markdown-testing_files/figure-gfm/unnamed-chunk-7-1.png)<!-- -->

### Stats table

| Race                    | plays | wins | WinsPerPlay | second | third | fourth | fifth | sixth |
| :---------------------- | ----: | ---: | ----------: | -----: | ----: | -----: | ----: | ----: |
| Arborec                 |  1232 |  228 |   0.1850649 |    240 |   270 |    210 |   176 |   108 |
| Barony of Letnev        |  1530 |  312 |   0.2039216 |    328 |   327 |    258 |   192 |   113 |
| Clan of Saar            |  1159 |  301 |   0.2597066 |    271 |   237 |    160 |   123 |    67 |
| Embers of Muaat         |  1125 |  166 |   0.1475556 |    258 |   247 |    222 |   144 |    88 |
| Emirates of Hacan       |  1965 |  428 |   0.2178117 |    474 |   453 |    353 |   172 |    85 |
| Federation of Sol       |  1987 |  543 |   0.2732763 |    463 |   428 |    319 |   144 |    90 |
| Ghosts of Creuss        |  1384 |  267 |   0.1929191 |    266 |   315 |    252 |   175 |   109 |
| L1Z1X Mindnet           |  1516 |  345 |   0.2275726 |    295 |   331 |    266 |   188 |    91 |
| Mentak Coalition        |  1389 |  254 |   0.1828654 |    295 |   331 |    262 |   166 |    81 |
| Naalu Collective        |  1286 |  352 |   0.2737170 |    295 |   230 |    215 |   116 |    78 |
| Nekro Virus             |  1225 |  209 |   0.1706122 |    259 |   247 |    233 |   162 |   115 |
| Sardakk N’orr           |  1086 |  159 |   0.1464088 |    199 |   247 |    232 |   152 |    97 |
| Universities of Jol-Nar |  1856 |  515 |   0.2774784 |    458 |   389 |    285 |   138 |    71 |
| Winnu                   |   505 |  129 |   0.2554455 |    104 |   104 |     87 |    52 |    29 |
| Xxcha Kingdom           |  1656 |  292 |   0.1763285 |    325 |   354 |    353 |   211 |   121 |
| Yin Brotherhood         |   919 |  192 |   0.2089227 |    182 |   208 |    158 |   112 |    67 |
| Yssaril Tribes          |  1302 |  300 |   0.2304147 |    280 |   274 |    225 |   155 |    68 |
