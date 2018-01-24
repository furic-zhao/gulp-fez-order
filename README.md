# gulp-fez-order

用于排序gulp文件流

## 使用方法

```
const contain = ['**/jquery.js', '**/fullpage.js', '**/mousewheel.js'];

const target = 'vendor-jquery.js';

gulp.src('./tmp/bower/**/*.js')
  .pipe(filter(contain))
  .pipe(concatOrder(contain))
  .pipe(concatJs(target))
  .pipe(uglify())
  .pipe(gulp.dest('/'))
```

> 文件流将会以字母或数字的降序排列。