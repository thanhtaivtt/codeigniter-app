## CodeIgniter + Blade Template + Eloquent ORM

### Requires

- php: >=5.5.9

### Instalation

Install the Illuminate Database,Codeigniter +Blade System + Taiscript package with Composer:

```sh
$ composer install
```

### Using the taiscript

**Example:**

```sh
$ php taiscript make:controller HomeController
```

-List: $ php taiscript help

### Using The Eloquent ORM

**Example:**

Model

```php
<?php
use \Illuminate\Database\Eloquent\Model as Eloquent;

class User extends Eloquent{
    protected $table = 'users';

}
```

Controller

```php
defined('BASEPATH') OR exit('No direct script access allowed');

class HomeController extends CI_Controller {

	public function index()
	{
		$this->load->model('user');

		$users = User::where('votes', '>', 1)->get();

	}
}
```
### Using The Blade Template

**Example:**

Controller

```php
defined('BASEPATH') OR exit('No direct script access allowed');

class HomeController extends CI_Controller {

	public function index()
	{
		$this->load->model('user');

		$data = User::where('votes', '>', 1)->get();

		$this->view('ViewName',['data' =>$data ]);
	}
}
```
### Documentation

- [CodeIgniter documentation](http://www.codeigniter.com/user_guide/)

- [Laravel framework - Eloquent documentation](https://laravel.com/docs/5.3/eloquent)

- [Laravel framework - Blade template documentation](https://laravel.com/docs/5.3/blade)

- [Others - Tutorial Others ](http:toidicode.com)

