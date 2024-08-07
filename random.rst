.. code:: ipython3

    import random

.. code:: ipython3

    horses = ["horse1", "horse2", "horse3", "horse4", "horse5", "horse6", "horse7", "horse8", "horse9", "horse10",
              "horse11", "horse12", "horse13", "horse14", "horse15", "horse16", "horse17", "horse18", "horse19", "horse20"]

.. code:: ipython3

    num_groups = 4

.. code:: ipython3

    random.shuffle(horses)

.. code:: ipython3

    horses_per_group = len(horses) // num_groups

.. code:: ipython3

    groups = [horses[i:i + horses_per_group] for i in range(0, len(horses), horses_per_group)]

.. code:: ipython3

    remaining_horses = len(horses) % num_groups
    for i in range(remaining_horses):
        groups[i].append(horses[-(i+1)])

.. code:: ipython3

    group_names = ["Control", "Laminitis", "Prophylactic", "Treatment"]

.. code:: ipython3

    for idx, group in enumerate(groups):
        print(f"{group_names[idx]} Group: {group}")


.. parsed-literal::

    Control Group: ['horse19', 'horse13', 'horse7', 'horse2', 'horse5']
    Laminitis Group: ['horse17', 'horse6', 'horse4', 'horse20', 'horse12']
    Prophylactic Group: ['horse16', 'horse9', 'horse8', 'horse11', 'horse10']
    Treatment Group: ['horse14', 'horse18', 'horse15', 'horse3', 'horse1']





