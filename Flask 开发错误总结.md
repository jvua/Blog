# Flask 开发错误总结

##### 第五章

错误信息如下：

```Python
UserWarning: SQLALCHEMY_TRACK_MODIFICATIONS adds significant overhead and will be disabled by default in the future.  Set it to True to suppress this warning.
  warnings.warn('SQLALCHEMY_TRACK_MODIFICATIONS adds significant overhead and will be disabled by default in the future.  Set it to True to suppress this warning.')
```

去flask_sqlalchemy的 __ init __.py 里面修改下面一行

```python
track_modifications = app.config.setdefault('SQLALCHEMY_TRACK_MODIFICATIONS', True)
```

