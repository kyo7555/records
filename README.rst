Records: SQL for Humans™
========================

----------

☤ 使用
------------
我们在执行插入或更新sql时，有时候需要知道插入/更新成功了多少条记录，而 records 原生不支持。故拉了一个版本过来，自己改了一下，增加了返回 affected_rows() 条数

.. code:: python

    import records

    db = records.Database('postgres://...')
    affected_rows = db.query('insert into xxx').affected_rows()

