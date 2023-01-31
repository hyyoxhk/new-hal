## new-hal

我想做一个hal层，暂时还没想好叫什么名字. 它类似于Android的hal层代码，但是我想用c代码
实现它，并集成在yocto上. 我熟读了linux 驱动层的代码，并理解了一部分其中的编码思想，我想
用那种模式去实现我的hal层

I want to make a hal layer, but I haven't decided what to call it yet. It is 
similar to Android's hal layer code, but I want to use c code realize it and 
integrate it on yocto. I have read the code of the linux driver layer and 
understood part of the coding ideas. I think use that mode to implement my hal layer

```c
struct hal_driver {
	const char *name;
	const char *mod_name;
	bool (*load)();
	bool (*unload)();
	bool (*isload)();
};

struct hal {
	struct hal_driver *driver;
};

hal_register(struct hal *hal);
```
