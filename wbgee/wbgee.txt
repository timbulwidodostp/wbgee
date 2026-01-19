# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Panel regression models fit with GEE (Generalized Estimating Equations) Use wbgee (panelr) With (In) R Software
install.packages("remotes")
remotes::install_github("cran/panelr")
install.packages("remotes")
install.packages("geepack")
library("geepack")
library("panelr")
# Estimates Panel regression models fit with GEE (Generalized Estimating Equations) Use wbgee (panelr) With (In) R Software
wbgee = read.csv("https://raw.githubusercontent.com/timbulwidodostp/wbgee/main/wbgee/wbgee.csv", sep = ";")
wbgee <- panel_data(wbgee, id = id, wave = t)
wbgee <- wbgee(lwage ~ lag(union) + wks | blk + fem | blk * lag(union), data = wbgee)
summary(wbgee)
# Panel regression models fit with GEE (Generalized Estimating Equations) Use wbgee (panelr) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished