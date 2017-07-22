class HomeController extends CI_Controller {
​
    public function index()
    {
        $this->load->model('user');
​
        $users = User::where('votes', '>', 1)->get();
​
    }
}
```
### Using The Blade Template
​
**Example:**
​
- Controller
​
```php
defined('BASEPATH') OR exit('No direct script access allowed');
​
class HomeController extends CI_Controller {
​
    public function index()
    {
        $this->load->model('user');
​
        $data = User::where('votes', '>', 1)->get();
​
        $this->view('ViewName',['data' =>$data ]);
    }
}
```
### Input
- In Controller:
```php
//get
$this->get('name');
​
//post
$this->post('name')
```
​
## Documentation
​
- [CodeIgniter documentation](http://www.codeigniter.com/user_guide/)
​
- [Laravel framework - Eloquent documentation](https://laravel.com/docs/5.3/eloquent)
​
- [Laravel framework - Blade template documentation](https://laravel.com/docs/5.3/blade)
​
- [Others - Tutorial Others ](http:toidicode.com)
​
