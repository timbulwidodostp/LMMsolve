# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Solve Linear Mixed Models using Restricted (residual) Maximum Likelihood (REML) Use LMMsolve (LMMsolver) With (In) R Software
install.packages("LMMsolver")
library("LMMsolver")
# Estimate Solve Linear Mixed Models using Restricted (residual) Maximum Likelihood (REML) Use LMMsolve (LMMsolver) With (In) R Software
LMMsolve_Data = read.csv("https://raw.githubusercontent.com/timbulwidodostp/LMMsolve/main/LMMsolve/LMMsolve.csv",sep = ";")
LMMsolve <- LMMsolve(fixed = yield ~ rep + gen, data = LMMsolve_Data)
LMMsolve_ <- LMMsolve(fixed = yield ~ rep, random = ~gen, data = LMMsolve_Data)
LMMsolve__ <- LMMsolve(fixed = yield ~ rep + gen, spline = ~spl1D(x = plot, nseg = 20), data = LMMsolve_Data)
summary(LMMsolve)
summary(LMMsolve_)
summary(LMMsolve__)
# Solve Linear Mixed Models using Restricted (residual) Maximum Likelihood (REML) Use LMMsolve (LMMsolver) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished