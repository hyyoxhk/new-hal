## new-hal

我想做一个hal层，暂时还没想好叫什么名字. 它类似于Android的hal层代码，但是我想用c代码
实现它，并集成在yocto上. 我熟读了linux 驱动层的代码，并理解了一部分其中的编码思想，我想
用那种模式去实现我的hal层

struct hal_driver {
	bool (*load)();
	bool (*unload)();
	bool (*isload)();
};

struct hal {
	struct hal_driver *driver;
};
