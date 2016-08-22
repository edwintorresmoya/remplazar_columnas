# remplazar_columnas
Remplaza el nombre de las columnas basado en una lista


a = data.frame(a=(gl(n = 4, k = 3, labels = c(2,4,6,8))), b= NA)
a
b = data.frame(t= c(2,4,6,8), y = c(100,200,300,400))
b
if (a$a == b$t) {b$y = a$b}
for (i in 1:nrow(a)) {
    for(j in 1:nrow(b) )
        if(a[i,]$a == b[j,]$t){a[i,]$b = b[j,]$y }
}
a
b[1,]$y
