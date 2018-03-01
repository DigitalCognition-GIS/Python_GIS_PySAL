Help on W in module pysal.weights.weights object:

class W(builtins.object)
 |  Spatial weights.
 |  
 |  Parameters
 |  ----------
 |  neighbors       : dictionary
 |                    key is region ID, value is a list of neighbor IDS
 |                    Example:  {'a':['b'],'b':['a','c'],'c':['b']}
 |  weights : dictionary
 |                    key is region ID, value is a list of edge weights
 |                    If not supplied all edge weights are assumed to have a weight of 1.
 |                    Example: {'a':[0.5],'b':[0.5,1.5],'c':[1.5]}
 |  id_order : list
 |                    An ordered list of ids, defines the order of
 |                    observations when iterating over W if not set,
 |                    lexicographical ordering is used to iterate and the
 |                    id_order_set property will return False.  This can be
 |                    set after creation by setting the 'id_order' property.
 |  silent_island_warning   : boolean
 |                          By default PySAL will print a warning if the
 |                          dataset contains any disconnected observations or
 |                          islands. To silence this warning set this
 |                          parameter to True.
 |  ids : list
 |                    values to use for keys of the neighbors and weights dicts
 |  
 |  Attributes
 |  ----------
 |  
 |  asymmetries         : list
 |                        of
 |  cardinalities       : dictionary
 |                        of
 |  diagW2              : array
 |                        of
 |  diagWtW             : array
 |                        of
 |  diagWtW_WW          : array
 |                        of
 |  histogram           : dictionary
:
 Examples
 |      --------
 |      >>> import pysal as ps
 |      >>> from pysal import W
 |      >>> neighbors={'first':['second'],'second':['first','third'],'third':['second']}
 |      >>> weights={'first':[1],'second':[1,1],'third':[1]}
 |      >>> w=W(neighbors,weights)
 |      >>> wsp=w.towsp()
 |      >>> isinstance(wsp, ps.weights.weights.WSP)
 |      True
 |      >>> wsp.n
 |      3
 |      >>> wsp.s0
 |      4
 |      
 |      See also
 |      --------
 |      WSP
 |  
 |  ----------------------------------------------------------------------
 |  Class methods defined here:
 |  
 |  from_WSP(WSP, silent_island_warning=True) from builtins.type
 |  
 |  from_file(path='', format=None, **kwargs) from builtins.type
 |  
 |  from_shapefile(*args, **kwargs) from builtins.type
 |  
 |  ----------------------------------------------------------------------
 |  Data descriptors defined here:
 |  
 |  __dict__
 |      dictionary for instance variables (if defined)
 |  
 |  __weakref__
 |      list of weak references to the object (if defined)
 |  
 |  asymmetries
 |      List of id pairs with asymmetric weights.
 |  
 |  cardinalities
 |      Number of neighbors for each observation.
:
 diagW2
 |      Diagonal of :math:`WW`.
 |      
 |      See Also
 |      --------
 |      trcW2
 |  
 |  diagWtW
 |      Diagonal of :math:`W^{'}W`.
 |      
 |      See Also
 |      --------
 |      trcWtW
 |  
 |  diagWtW_WW
 |      Diagonal of :math:`W^{'}W + WW`.
 |  
 |  histogram
 |      Cardinality histogram as a dictionary where key is the id and
 |      value is the number of neighbors for that unit.
 |  
 |  id2i
 |      Dictionary where the key is an ID and the value is that ID's
 |      index in W.id_order.
 |  
 |  id_order
 |      Returns the ids for the observations in the order in which they
 |      would be encountered if iterating over the weights.
 |  
 |  id_order_set
 |      Returns True if user has set id_order, False if not.
 |      
 |      Examples
 |      --------
 |      >>> from pysal import lat2W
 |      >>> w=lat2W()
 |      >>> w.id_order_set
 |      True
 |  
 |  islands
:
|      True
 |  
 |  islands
 |      List of ids without any neighbors.
 |  
 |  max_neighbors
 |      Largest number of neighbors.
 |  
 |  mean_neighbors
 |      Average number of neighbors.
 |  
 |  min_neighbors
 |      Minimum number of neighbors.
 |  
 |  n
 |      Number of units.
 |  
 |  neighbor_offsets
 |      Given the current id_order, neighbor_offsets[id] is the offsets of the
 |      id's neighbors in id_order.
 |      
 |      Returns
 |      -------
 |      list
 |              offsets of the id's neighbors in id_order
 |      
 |      Examples
 |      --------
 |      >>> from pysal import W
 |      >>> neighbors={'c': ['b'], 'b': ['c', 'a'], 'a': ['b']}
 |      >>> weights ={'c': [1.0], 'b': [1.0, 1.0], 'a': [1.0]}
 |      >>> w=W(neighbors,weights)
 |      >>> w.id_order = ['a','b','c']
 |      >>> w.neighbor_offsets['b']
 |      [2, 0]
 |      >>> w.id_order = ['b','a','c']
 |      >>> w.neighbor_offsets['b']
 |      [2, 1]
 |  
 |  nonzero
 pct_nonzero
 |      Percentage of nonzero weights.
 |  
 |  s0
 |      s0 is defined as
 |      
 |      .. math::
 |      
 |             s0=\sum_i \sum_j w_{i,j}
 |  
 |  s1
 |      s1 is defined as
 |      
 |      .. math::
 |      
 |             s1=1/2 \sum_i \sum_j (w_{i,j} + w_{j,i})^2
 |  
 |  s2
 |      s2 is defined as
 |      
 |      .. math::
 |      
 |              s2=\sum_j (\sum_i w_{i,j} + \sum_i w_{j,i})^2
 |  
 |  s2array
 |      Individual elements comprising s2.
 |      
 |      See Also
 |      --------
 |      s2
 |  
 |  sd
 |      Standard deviation of number of neighbors.
 |  
 |  sparse
 |      Sparse matrix object.
 |      
 |      For any matrix manipulations required for w, w.sparse should be
 |      used. This is based on scipy.sparse.
 |  
 |  transform
:


