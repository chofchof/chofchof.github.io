# Unix & Linux Stack Exchange

## Bash

  - [Why is pattern ``command || true`` useful?](https://unix.stackexchange.com/questions/325705/why-is-pattern-command-true-useful)

# Stack Overflow

## [numpy](https://stackoverflow.com/questions/tagged/numpy)

  - [numpy: Efficiently avoid 0s when taking log(matrix)](https://stackoverflow.com/questions/21752989/numpy-efficiently-avoid-0s-when-taking-logmatrix)
  
  > **Answer by John Zwinck**
  >
  > We can use masked arrays for this:
  >
       x = array([[1,0], [2,3]])
       log_x = np.ma.log(x).filled(0)

## [matplotlib](https://stackoverflow.com/questions/tagged/matplotlib)

  - [Prevent matplotlib statefulness](https://stackoverflow.com/questions/28631741/prevent-matplotlib-statefulness)
  
  > **Answer by Joe Kington**
  >
  > Normally, when you call `plt.figure()`, it:
  >
  > 1. Creates the figure object that's returned
  > 2. Creates a `FigureManager` for that figure using the appropriate backend
  > 3. The figure manager creates a `FigureCanvas`, gui window (as needed), and `NavigationToolbar2` (zoom buttons, etc)
  > 4. The figure manager instance is then added to `_pylab_helpers.Gcf`'s list of figures.
  >
  > It's this last step that we want to bypass.
