# PullToRefresh

    Android PullToRefresh

#Usage

##Layout


``` xml
  <com.chico.pulltorefresh.library.PullToRefreshLayout
        android:id="@+id/pull_refresh_layout"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:background="@color/bg_color"
        android:orientation="vertical" >

        <include layout="@layout/refresh_head" />
        <!-- 支持所有实现Pullable接口的View -->

        <com.chico.pulltorefresh.library.PullableGridView
            android:id="@+id/pull_refresh_grid"
            android:layout_width="match_parent"
            android:layout_height="match_parent"
            android:horizontalSpacing="5dip"
            android:numColumns="2"
            android:scrollbars="none"
            android:stretchMode="columnWidth"
            android:verticalSpacing="5dip" />

        <include layout="@layout/load_more" />
    </com.chico.pulltorefresh.library.PullToRefreshLayout>
```
```java
	mPullToRefreshLayout = (PullToRefreshLayout) findViewById(R.id.pull_refresh_layout);
	mPullToRefreshLayout.setOnRefreshListener(new OnRefreshListener() {

		@Override
		public void onRefresh(PullToRefreshLayout pullToRefreshLayout) {
			//loadDate
            pullToRefreshLayout.refreshFinish(PullToRefreshLayout.SUCCEED);
		}

		@Override
		public void onLoadMore(PullToRefreshLayout pullToRefreshLayout) {
			//loadDate
			 pullToRefreshLayout.loadmoreFinish(PullToRefreshLayout.SUCCEED);
		}
	});

    gridView = (PullableGridView) findViewById(R.id.pull_refresh_grid);

```
	
#Contributors


*(https://github.com/jingchenUSTC/PullToRefreshAndLoad)

