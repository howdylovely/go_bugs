Question:
log.Fatal(server.ListenAndServe());

Bugs:
panic: runtime error: invalid memory address or nil pointer dereference

resovled:
打印函数传递的参数发现确实有空值，给参数正确赋值就能解决。
```bash
	err := server.ListenAndServe()
	if err != nil {
		log.Fatal(err)
	}
``
