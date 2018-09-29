# dataStructure_python
#
# 1. 评估算法的性能
# 
    当选择一个算法的时候，我们必须解决时间空间平衡的问题。通常情况下，可能会选择以空间（额外的内存）换取时间的做法，
    也有可能选择以时间换取空间（节约内存）的做法。
    
    
#   1.1度量算法的运行时间
    一个度量运行时间的例子：
    import time
    problemsize = 10000000
    print("%12s%16s"%("Problem Size","seconds"))
    for count in range(4):
        # 开始时间
        start = time.time()
        work = 1
        for x in range(problemsize):
            work+=1
            work-=1
        #时间间隔
        elapsed = time.time()-start
        print("%12d%16.3f"%(problemsize,elapsed))
        problemsize *=2
#    
    根据运行结果：
    Problem Size         seconds
    10000000             2.702
    20000000             3.366
    40000000             7.603
    80000000             12.719
    我们大致可以推测出，随着问题规模的扩大，运行时间也越来越长。
