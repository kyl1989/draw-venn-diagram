# draw-venn-diagram
#how to draw a venn diagram


install.packages("VennDiagram")
library(VennDiagram)

##################################
#知道集合，绘制韦恩图：venn.diagram()
#example:3组
A = 20:150
B = 50:150
C = 10:50
venn.diagram(x = list(A = A, B = B, C = C), filename = "venn.png", alpha = c(0.9, 0.9, 0.9),
scaled = FALSE,
col=c('#115C2F','#6954A4','#AF1F24'), fill=c('#ABB9A7','#C5BEDE','#E3B3A2'))


##################################
#仅知道集合及交集大小，绘制韦恩图的函数。
#2组：draw.pairwise.venn
#3组：draw.triple.venn
#4组：draw.quad.venn
#5组：draw.quintuple.venn

#example:2组
draw.pairwise.venn(area1 = 293, area2 = 330, cross.area = 285, category = c('aUC', 'iUC'),
scaled = FALSE,
fill = c('deepskyblue', 'mediumpurple'), col = c('#819DD1', '#6954A4'))

#example:3组
draw.triple.venn(area1=Length_A, area2=Length_B, area3=Length_C,
n12=Length_AB, n23=Length_BC, n13=Length_AC, n123=Length_ABC,
category = c('A','B','C'),
scaled = FALSE,
col=c('#115C2F','#6954A4','#AF1F24'), fill=c('#ABB9A7','#C5BEDE','#E3B3A2'))
