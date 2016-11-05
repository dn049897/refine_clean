
> refine_original <- read.csv("~/Desktop/refine_original.csv")
>   View(refine_original)
> brand <-refine_original
> print(brand)
company Product.code...number             address   city
1    Phillips                   p-5 Groningensingel 147 arnhem
2    phillips                  p-43 Groningensingel 148 arnhem
3     philips                   x-3 Groningensingel 149 arnhem
4     phllips                  x-34 Groningensingel 150 arnhem
5     phillps                  x-12 Groningensingel 151 arnhem
6    phillipS                  p-23 Groningensingel 152 arnhem
7        akzo                  v-43   Leeuwardenweg 178 arnhem
8        Akzo                  v-12   Leeuwardenweg 179 arnhem
9        AKZO                   x-5   Leeuwardenweg 180 arnhem
10       akz0                  p-34   Leeuwardenweg 181 arnhem
11      ak zo                   q-5   Leeuwardenweg 182 arnhem
12       akzo                   q-9   Leeuwardenweg 183 arnhem
13       akzo                   x-8   Leeuwardenweg 184 arnhem
14   phillips                  p-56   Delfzijlstraat 54 arnhem
15    fillips                  v-67   Delfzijlstraat 55 arnhem
16     phlips                  v-21   Delfzijlstraat 56 arnhem
17 Van Houten                  x-45   Delfzijlstraat 57 arnhem
18 van Houten                  v-56   Delfzijlstraat 58 arnhem
19 van houten                  v-65   Delfzijlstraat 59 arnhem
20 van houten                  x-21   Delfzijlstraat 60 arnhem
21 Van Houten                  p-23   Delfzijlstraat 61 arnhem
22    unilver                   x-3      Jourestraat 23 arnhem
23   unilever                   q-4      Jourestraat 24 arnhem
24   Unilever                   q-6      Jourestraat 25 arnhem
25   unilever                   q-8      Jourestraat 26 arnhem
country             name
1  the netherlands    dhr p. jansen
2  the netherlands    dhr p. hansen
3  the netherlands    dhr j. Gansen
4  the netherlands    dhr p. mansen
5  the netherlands   dhr p. fransen
6  the netherlands  dhr p. franssen
7  the netherlands    dhr p. bansen
8  the netherlands    dhr p. vansen
9  the netherlands   dhr p. bransen
10 the netherlands   dhr p. janssen
11 the netherlands  mevr l.  rokken
12 the netherlands  mevr l.  lokken
13 the netherlands  mevr l.  mokken
14 the netherlands  mevr l.  mokken
15 the netherlands  mevr l.  mokken
16 the netherlands  mevr l.  mokken
17 the netherlands  mevr l.  sokken
18 the netherlands  mevr l.  wokken
19 the netherlands  mevr l.  kokken
20 the netherlands  mevr l.  Bokken
21 the netherlands  mevr l.  dokken
22 the netherlands  mevr l.  gokken
23 the netherlands mevr l.  stokken
24 the netherlands  mevr l.  rokken
25 the netherlands  mevr l.  rokken
> brand$company <- gsub("fillips|phillips|phillipS|Phillips|phillps|phlips|phllips","philips",brand$company)
> brand$company <- gsub("AKZO|Akzo|akzO|akz0|ak zo","akzo",brand$company)
>brand$company <- gsub("Van Houten|van Houten|Van houten","van houten",brand$company)
> brand$company <- gsub("unilver|Unilever","unilever",brand$company)
> install.packages("tidyr")
trying URL 'https://cran.rstudio.com/bin/macosx/mavericks/contrib/3.3/tidyr_0.6.0.tgz'
Content type 'application/x-gzip' length 549152 bytes (536 KB)
==================================================
  downloaded 536 KB


The downloaded binary packages are in
/var/folders/kh/12yqtqmj175b6fg000h9m1740000gn/T//RtmpWY93qR/downloaded_packages
> library(tidyr)
> separate(brand,Product.code...number, into = c("product_code","product_number"), sep = "-")
> brand$product_category <- brand$product_code
> brand <- separate(brand,Product.code...number, into = c("product_code","product_number"), sep = "-")
> brand$product_category <- brand$product_code
> brand$product_category <- gsub("p","Smartphone",brand$product_category)
> brand$product_category <- gsub("v","TV",brand$product_category)
> brand$product_category <- gsub("x","Laptop",brand$product_category)
> brand$product_category <- gsub("q","Tablet",brand$product_category)
brand$full_address <- paste(brand$address,brand$city,brand$country,sep = ",")
brand$company_unilever <- brand$company
>brand$company_philips <- brand$company
>brand$company_akzo <- brand$company
>brand$company_van_houten <- brand$company
>brand$company_philips<- gsub("akzo|van houten|unilever","0",brand$company_philips)
>brand$company_philips <- gsub("philips","1",brand$company_philips)
>brand$company_akzo <- gsub("philips|van houten|unilever","0",brand$company_akzo)
>brand$company_akzo <- gsub("akzo","1",brand$company_akzo)
brand$company_van_houten <- gsub("van houten","1",brand$company_van_houten)
>brand$company_van_houten <- gsub("philips|akzo|unilever","0",brand$company_van_houten)
>brand$company_unilever <- gsub("van houten|philips|akzo","0",brand$company_unilever)
>brand$company_unilever <- gsub("unilever","1",brand$company_unilever)
brand$product_smartphone <- brand$product_category
brand$product_smartphone <- gsub("Smartphone","1",brand$product_smartphone)
brand$product_smartphone <- gsub("Tablet|TV|Laptop","0",brand$product_smartphone)
brand$product_tv <- brand$product_category
> brand$product_tv <- gsub("TV","1",brand$product_tv)
>brand$product_tv <- gsub("Tablet|Laptop|Smartphone","0",brand$product_tv)
brand$laptop <- brand$product_category
> brand$laptop <- gsub("Laptop", "1",brand$laptop)
> brand$laptop <- gsub("TV|Smartphone|Tablet","0",brand$laptop)
brand$tablet <- brand$product_category
> brand$tablet <- gsub("Tablet","1",brand$tablet)
> brand$tablet <- gsub("TV|Laptop|Smartphone", "0",brand$tablet)
> brand$company_unilever <- gsub("van houten|philips|akzo","0",brand$company_unilever)
> brand$company_unilever <- gsub("unilever","1",brand$company_unilever)
> brand$product_smartphone <- brand$product_category
> brand$product_smartphone <- gsub("Smartphone","1",brand$product_smartphone)
> brand$product_smartphone <- gsub("Laptop","0",brand$product_smartphone)
> brand$product_smartphone <- gsub("Tablet|TV","0",brand$product_smartphone)
> brand$product_tv <- brand$product_category
> brand$product_tv <- gsub("TV","1",brand$product_tv)
> brand$product_tv <- gsub("Tablet|Laptop|Smartphone","0",brand$product_tv)
> brand$laptop <- brand$product_category
> brand$laptop <- gsub("Laptop", "1",brand$laptop)
> brand$laptop <- gsub("TV|Smartphone|Tablet","0",brand$laptop)
> brand$tablet <- brand$product_category
> brand$tablet <- gsub("Tablet","1",brand$tablet)
> brand$tablet <- gsub("TV|Laptop|Smartphone", "0",brand$tablet)
> > print(brand)
company product_code product_number             address   city         country
1     philips            p              5 Groningensingel 147 arnhem the netherlands
2     philips            p             43 Groningensingel 148 arnhem the netherlands
3     philips            x              3 Groningensingel 149 arnhem the netherlands
4     philips            x             34 Groningensingel 150 arnhem the netherlands
5     philips            x             12 Groningensingel 151 arnhem the netherlands
6     philips            p             23 Groningensingel 152 arnhem the netherlands
7        akzo            v             43   Leeuwardenweg 178 arnhem the netherlands
8        akzo            v             12   Leeuwardenweg 179 arnhem the netherlands
9        akzo            x              5   Leeuwardenweg 180 arnhem the netherlands
10       akzo            p             34   Leeuwardenweg 181 arnhem the netherlands
11       akzo            q              5   Leeuwardenweg 182 arnhem the netherlands
12       akzo            q              9   Leeuwardenweg 183 arnhem the netherlands
13       akzo            x              8   Leeuwardenweg 184 arnhem the netherlands
14    philips            p             56   Delfzijlstraat 54 arnhem the netherlands
15    philips            v             67   Delfzijlstraat 55 arnhem the netherlands
16    philips            v             21   Delfzijlstraat 56 arnhem the netherlands
17 van houten            x             45   Delfzijlstraat 57 arnhem the netherlands
18 van houten            v             56   Delfzijlstraat 58 arnhem the netherlands
19 van houten            v             65   Delfzijlstraat 59 arnhem the netherlands
20 van houten            x             21   Delfzijlstraat 60 arnhem the netherlands
21 van houten            p             23   Delfzijlstraat 61 arnhem the netherlands
22   unilever            x              3      Jourestraat 23 arnhem the netherlands
23   unilever            q              4      Jourestraat 24 arnhem the netherlands
24   unilever            q              6      Jourestraat 25 arnhem the netherlands
25   unilever            q              8      Jourestraat 26 arnhem the netherlands
name product_category                               full_address company_philips
1     dhr p. jansen       Smartphone Groningensingel 147,arnhem,the netherlands               1
2     dhr p. hansen       Smartphone Groningensingel 148,arnhem,the netherlands               1
3     dhr j. Gansen           Laptop Groningensingel 149,arnhem,the netherlands               1
4     dhr p. mansen           Laptop Groningensingel 150,arnhem,the netherlands               1
5    dhr p. fransen           Laptop Groningensingel 151,arnhem,the netherlands               1
6   dhr p. franssen       Smartphone Groningensingel 152,arnhem,the netherlands               1
7     dhr p. bansen               TV   Leeuwardenweg 178,arnhem,the netherlands               0
8     dhr p. vansen               TV   Leeuwardenweg 179,arnhem,the netherlands               0
9    dhr p. bransen           Laptop   Leeuwardenweg 180,arnhem,the netherlands               0
10   dhr p. janssen       Smartphone   Leeuwardenweg 181,arnhem,the netherlands               0
11  mevr l.  rokken           Tablet   Leeuwardenweg 182,arnhem,the netherlands               0
12  mevr l.  lokken           Tablet   Leeuwardenweg 183,arnhem,the netherlands               0
13  mevr l.  mokken           Laptop   Leeuwardenweg 184,arnhem,the netherlands               0
14  mevr l.  mokken       Smartphone   Delfzijlstraat 54,arnhem,the netherlands               1
15  mevr l.  mokken               TV   Delfzijlstraat 55,arnhem,the netherlands               1
16  mevr l.  mokken               TV   Delfzijlstraat 56,arnhem,the netherlands               1
17  mevr l.  sokken           Laptop   Delfzijlstraat 57,arnhem,the netherlands               0
18  mevr l.  wokken               TV   Delfzijlstraat 58,arnhem,the netherlands               0
19  mevr l.  kokken               TV   Delfzijlstraat 59,arnhem,the netherlands               0
20  mevr l.  Bokken           Laptop   Delfzijlstraat 60,arnhem,the netherlands               0
21  mevr l.  dokken       Smartphone   Delfzijlstraat 61,arnhem,the netherlands               0
22  mevr l.  gokken           Laptop      Jourestraat 23,arnhem,the netherlands               0
23 mevr l.  stokken           Tablet      Jourestraat 24,arnhem,the netherlands               0
24  mevr l.  rokken           Tablet      Jourestraat 25,arnhem,the netherlands               0
25  mevr l.  rokken           Tablet      Jourestraat 26,arnhem,the netherlands               0
company_akzo company_van_houten company_unilever product_smartphone product_tv laptop tablet
1             0                  0                0                  1          0      0      0
2             0                  0                0                  1          0      0      0
3             0                  0                0                  0          0      1      0
4             0                  0                0                  0          0      1      0
5             0                  0                0                  0          0      1      0
6             0                  0                0                  1          0      0      0
7             1                  0                0                  0          1      0      0
8             1                  0                0                  0          1      0      0
9             1                  0                0                  0          0      1      0
10            1                  0                0                  1          0      0      0
11            1                  0                0                  0          0      0      1
12            1                  0                0                  0          0      0      1
13            1                  0                0                  0          0      1      0
14            0                  0                0                  1          0      0      0
15            0                  0                0                  0          1      0      0
16            0                  0                0                  0          1      0      0
17            0                  1                0                  0          0      1      0
18            0                  1                0                  0          1      0      0
19            0                  1                0                  0          1      0      0
20            0                  1                0                  0          0      1      0
21            0                  1                0                  1          0      0      0
22            0                  0                1                  0          0      1      0
23            0                  0                1                  0          0      0      1
24            0                  0                1                  0          0      0      1
25            0                  0                1                  0          0      0      1
