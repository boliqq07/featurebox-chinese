Backforward
======================

Select by Backforward
::

>>> from sklearn.datasets import fetch_california_housing
>>> from sklearn.svm import SVR
>>> from featurebox.selection.backforward import BackForward
>>> X,y = fetch_california_housing(return_X_y=True)
>>> svr= SVR()
>>> bf = BackForward(svr, primary_feature=4, random_state=1)
>>> new_x = bf.fit_transform(X,y)
>>> bf.support_
>>> array([False, False, False, False, False, False, False, False, False, False,  True, False,  True])
