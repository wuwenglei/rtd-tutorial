Random Over-sampling
=====

.. _installation:

Installation
------------

To use Lumache, first install it using pip:

.. code-block:: console

   (.venv) $ pip install lumache

Creating recipes
----------------

To retrieve a list of random ingredients,
you can use the ``lumache.get_random_ingredients()`` function:

.. autofunction:: lumache.get_random_ingredients

The ``kind`` parameter should be either ``"meat"``, ``"fish"``,
or ``"veggies"``. Otherwise, :py:func:`lumache.get_random_ingredients`
will raise an exception.

.. autoexception:: lumache.InvalidKindError

For example:

>>> import lumache
>>> lumache.get_random_ingredients()
['shells', 'gorgonzola', 'parsley']

.. method:: ro(data, y, samp_method ="balance", drop_na_col =True, drop_na_row = True, replace = True, manual_perc = False, perc_o = -1, rel_thres = 0.5, rel_method = "auto", rel_xtrm_type = "both", rel_coef = 1.5, rel_ctrl_pts_rg = None) 
    Random Over-sampling is an over-sampling method that synthesizes new samples by randomly copying minority samples.
    :param data: Pandas dataframe, the dataset to re-sample.
    :type data: :term:`Pandas dataframe`
    :param str y: Name of the target variable.
