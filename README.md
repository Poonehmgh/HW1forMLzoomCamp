df['Engine Cylinders'].median()


a = df[df.Make == 'Lotus']



a[['Engine HP', 'Engine Cylinders']].drop_duplicates()




x = a[['Engine HP', 'Engine Cylinders']].drop_duplicates().values




xt = x.T



def question7(x,xt):
    assert x.shape[1]== xt.shape[0]
    n = x.shape[0]
    m = x.shape[1]
    result=np.zeros(n)
    for i in range (n):
        for j in range (m):
           result[i] = result[i] + x[i][j] * xt[j][i]
        
    return result
xtx = question7(x,xt)
