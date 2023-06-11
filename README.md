# datascience-pandas
plt.figure()
plt.title('Materials thermal comparison')

bspl=interpolate.make_interp_spline(aluminium.Iterations,aluminium['temp'],k=3)
x=np.linspace(aluminium.Iterations.min(),aluminium.Iterations.max(),20 )
y=bspl(x)
plt.plot(x,y, 'b', label='aluminium')
