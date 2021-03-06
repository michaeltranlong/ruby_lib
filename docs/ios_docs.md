##### [load_settings](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/appium.rb#L45) 

> def load_settings(opts = {})

Load arbitrary text ([toml format](https://github.com/toml-lang/toml))
The toml is parsed by https://github.com/fbernier/tomlrb .

```
[caps]
app = "path/to/app"

[appium_lib]
port = 8080
```

:app is expanded
:require is expanded
all keys are converted to symbols

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Hash] opts - file: '/path/to/appium.txt', verbose: true

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[hash] the symbolized hash with updated :app and :require keys

--

##### [load_appium_txt](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/appium.rb#L79) 

> def load_settings(opts = {})

Load arbitrary text ([toml format](https://github.com/toml-lang/toml))
The toml is parsed by https://github.com/fbernier/tomlrb .

```
[caps]
app = "path/to/app"

[appium_lib]
port = 8080
```

:app is expanded
:require is expanded
all keys are converted to symbols

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Hash] opts - file: '/path/to/appium.txt', verbose: true

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[hash] the symbolized hash with updated :app and :require keys

--

##### [expand_required_files](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/appium.rb#L84) 

> def expand_required_files(base_dir, file_paths)



__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] base_dir - parent directory of loaded appium.txt (toml)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] file_paths - 

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array] list of require files as an array, nil if require doesn't exist

--

##### [promote_singleton_appium_methods](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/appium.rb#L126) 

> def promote_singleton_appium_methods(modules, driver = $driver)

This method is intended to work with page objects that share
a common module. For example, Page::HomePage, Page::SignIn
those could be promoted on with Appium.promote_singleton_appium_methods Page

If you are promoting on an individual class then you should use
Appium.promote_appium_methods instead. The singleton method is intended
only for the shared module use case.

if modules is a module instead of an array, then the constants of
that module are promoted on.
otherwise, the array of modules will be used as the promotion target.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<Module>] modules - An array of modules

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Driver] driver - A driver to extend for

--

##### [promote_appium_methods](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/appium.rb#L181) 

> def promote_appium_methods(class_array, driver = $driver)

Promote appium methods to class instance methods

To promote methods to all classes:

It's better to promote on specific classes instead of Object

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<Class>] class_array - An array of classes

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Driver] driver - A driver to extend for

--

##### [global_webdriver_http_sleep](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L24) 

> def global_webdriver_http_sleep

The amount to sleep in seconds before every webdriver http call.

--

##### [global_webdriver_http_sleep=](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L24) 

> def global_webdriver_http_sleep=(value)

The amount to sleep in seconds before every webdriver http call.

--

##### [sauce](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L27) 

> def sauce

SauceLab's settings

--

##### [sauce_username](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L30) 

> def sauce_username

Username for use on Sauce Labs. Set `false` to disable Sauce, even when SAUCE_USERNAME is in ENV.
same as @sauce.username

--

##### [sauce_access_key](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L33) 

> def sauce_access_key

Access Key for use on Sauce Labs. Set `false` to disable Sauce, even when SAUCE_ACCESS_KEY is in ENV.
same as @sauce.access_key

--

##### [sauce_endpoint](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L36) 

> def sauce_endpoint

Override the Sauce Appium endpoint to allow e.g. TestObject tests
same as @sauce.endpoint

--

##### [caps](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L39) 

> def caps

from Core

--

##### [custom_url](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L40) 

> def custom_url

Returns the value of attribute custom_url

--

##### [export_session](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L41) 

> def export_session

Returns the value of attribute export_session

--

##### [default_wait](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L42) 

> def default_wait

Returns the value of attribute default_wait

--

##### [appium_port](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L43) 

> def appium_port

Returns the value of attribute appium_port

--

##### [appium_device](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L44) 

> def appium_device

Returns the value of attribute appium_device

--

##### [automation_name](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L45) 

> def automation_name

Returns the value of attribute automation_name

--

##### [listener](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L46) 

> def listener

Returns the value of attribute listener

--

##### [http_client](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L47) 

> def http_client

Returns the value of attribute http_client

--

##### [appium_wait_timeout](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L48) 

> def appium_wait_timeout

Returns the value of attribute appium_wait_timeout

--

##### [appium_wait_interval](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L49) 

> def appium_wait_interval

Returns the value of attribute appium_wait_interval

--

##### [appium_server_status](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L52) 

> def appium_server_status

Appium's server version

--

##### [appium_debug](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L54) 

> def appium_debug

Boolean debug mode for the Appium Ruby bindings

--

##### [driver](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L57) 

> def driver

Returns the driver

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Driver] the driver

--

##### [core](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L59) 

> def core

Instance of Appium::Core::Driver

--

##### [initialize](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L110) 

> def initialize(opts = {}, global_driver = nil)

Creates a new driver. The driver is defined as global scope by default.
We can avoid defining global driver.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Object] opts - A hash containing various options.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Bool] global_driver - A bool require global driver before initialize.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Driver] 

--

##### [driver_attributes](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L215) 

> def driver_attributes

Returns a hash of the driver attributes

--

##### [device_is_android?](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L234) 

> def device_is_android?



__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Boolean] 

--

##### [device_is_ios?](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L238) 

> def device_is_ios?



__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Boolean] 

--

##### [device_is_windows?](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L242) 

> def device_is_windows?



__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Boolean] 

--

##### [automation_name_is_uiautomator2?](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L248) 

> def automation_name_is_uiautomator2?

Return true if automationName is 'uiautomator2'

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Boolean] 

--

##### [automation_name_is_espresso?](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L254) 

> def automation_name_is_espresso?

Return true if automationName is 'Espresso'

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Boolean] 

--

##### [automation_name_is_xcuitest?](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L260) 

> def automation_name_is_xcuitest?

Return true if automationName is 'XCUITest'

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Boolean] 

--

##### [check_server_version_xcuitest](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L267) 

> def check_server_version_xcuitest

Return true if the target Appium server is over REQUIRED_VERSION_XCUITEST.
If the Appium server is under REQUIRED_VERSION_XCUITEST, then error is raised.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Boolean] 

--

##### [appium_server_version](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L288) 

> def appium_server_version

Returns the server's version info

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Hash] 

--

##### [platform_version](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L298) 

> def platform_version

Return the platform version as an array of integers

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<Integer>] 

--

##### [appium_client_version](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L317) 

> def appium_client_version

Returns the client's version info

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Hash] 

--

##### [absolute_app_path](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L329) 

> def self.absolute_app_path(opts)

Converts app_path to an absolute path.

opts is the full options hash (caps and appium_lib). If server_url is set
then the app path is used as is.

if app isn't set then an error is raised.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] APP_PATH as an absolute path

--

##### [server_url](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L362) 

> def server_url

Get the server url

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] the server url

--

##### [restart](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L370) 

> def restart

Restarts the driver

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Driver] the driver

--

##### [screenshot](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L383) 

> def screenshot(png_save_path)

Takes a png screenshot and saves to the target path.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] png_save_path - the full path to save the png

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[nil] 

--

##### [driver_quit](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L389) 

> def driver_quit

Quits the driver

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[void] 

--

##### [quit_driver](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L392) 

> def driver_quit

Quits the driver

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[void] 

--

##### [window_size](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L403) 

> def window_size

Get the device window's size.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Selenium::WebDriver::Dimension] 

--

##### [start_driver](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L432) 

> def start_driver(http_client_ops =

Creates a new global driver and quits the old one if it exists.
You can customise http_client as the following

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Hash] http_client_ops - a customizable set of options

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Selenium::WebDriver] the new global driver

--

##### [set_implicit_wait](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L456) 

> def set_implicit_wait(wait)

To ignore error for Espresso Driver

--

##### [no_wait](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L466) 

> def no_wait

Set implicit wait to zero.

--

##### [set_wait](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L480) 

> def set_wait(timeout = nil)

Set implicit wait. Default to @core.default_wait.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Integer] timeout - the timeout in seconds

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[void] 

--

##### [exists](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L497) 

> def exists(pre_check = 0, post_check = @core.default_wait)

Returns existence of element.

Example:

exists { button('sign in') } ? puts('true') : puts('false')

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Integer] pre_check - The amount in seconds to set the
wait to before checking existence

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Integer] post_check - The amount in seconds to set the
wait to after checking existence

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Boolean] 

--

##### [execute_script](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L521) 

> def execute_script(script, *args)

The same as @driver.execute_script

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] script - The script to execute

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[*args] args - The args to pass to the script

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Object] 

--

##### [find_elements](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L543) 

> def find_elements(*args)

Calls @driver.find_elements_with_appium

If you call `Appium.promote_appium_methods`, you can call `find_elements` directly.

If you call `Appium.promote_appium_methods`, you can call `find_elements` directly.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[*args] args - The args to use

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<Element>] Array is empty when no elements are found.

--

##### [find_element](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L558) 

> def find_element(*args)

Calls @driver.find_element

If you call `Appium.promote_appium_methods`, you can call `find_element` directly.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[*args] args - The args to use

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] 

--

##### [set_location](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L571) 

> def set_location(opts = {})

Calls @driver.set_location

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Hash] opts - consisting of:

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Selenium::WebDriver::Location] the location constructed by the selenium webdriver

--

##### [x](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/driver.rb#L581) 

> def x

Quit the driver and Pry.
quit and exit are reserved by Pry.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[void] 

--

##### [username](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/sauce_labs.rb#L4) 

> def username

Username for use on Sauce Labs. Set `false` to disable Sauce, even when SAUCE_USERNAME is in ENV.

--

##### [access_key](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/sauce_labs.rb#L6) 

> def access_key

Access Key for use on Sauce Labs. Set `false` to disable Sauce, even when SAUCE_ACCESS_KEY is in ENV.

--

##### [endpoint](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/sauce_labs.rb#L8) 

> def endpoint

Override the Sauce Appium endpoint to allow e.g. TestObject tests. Default is 'ondemand.saucelabs.com:443/wd/hub'.

--

##### [initialize](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/sauce_labs.rb#L33) 

> def initialize(appium_lib_opts)

Create a SauceLabs instance to manage sauce labs related attributes.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Hash] appium_lib_opts - Appium library parameter

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Appium::SauceLabs] 

--

##### [sauce_server_url?](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/sauce_labs.rb#L53) 

> def sauce_server_url?

Return true if an instance of Appium::SauceLabs has sauce_username and sauce_access_key.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Boolean] 

--

##### [server_url](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/sauce_labs.rb#L66) 

> def server_url

Return a particular server url to access to. Default is the local address.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] 

--

##### [get_log](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/log.rb#L11) 

> def get_log(type)



__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String|Hash] type - You can get particular type's logs.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[[Selenium::WebDriver::LogEntry]] A list of logs data.

--

##### [get_available_log_types](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/log.rb#L23) 

> def get_available_log_types

Get a list of available log types

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[[String]] A list of available log types.

--

##### [initialize](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/wait.rb#L6) 

> def initialize(opts = {})



__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Wait] a new instance of Wait

--

##### [wait_true](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/wait.rb#L34) 

> def wait_true(opts = {})

Check every interval seconds to see if yield returns a truthy value.
Note this isn't a strict boolean true, any truthy value is accepted.
false and nil are considered failures.
Give up after timeout seconds.

Wait code from the selenium Ruby gem
https://github.com/SeleniumHQ/selenium/blob/cf501dda3f0ed12233de51ce8170c0e8090f0c20/rb/lib/selenium/webdriver/common/wait.rb

If only a number is provided then it's treated as the timeout value.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Hash] opts - Options

--

##### [wait](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/wait.rb#L57) 

> def wait(opts = {})

Check every interval seconds to see if yield doesn't raise an exception.
Give up after timeout seconds.

Wait code from the selenium Ruby gem
https://github.com/SeleniumHQ/selenium/blob/cf501dda3f0ed12233de51ce8170c0e8090f0c20/rb/lib/selenium/webdriver/common/wait.rb

If only a number is provided then it's treated as the timeout value.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Hash] opts - Options

--

##### [ignore](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L16) 

> def ignore

Return yield and ignore any exceptions.

--

##### [back](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L23) 

> def back

Navigate back.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[void] 

--

##### [session_id](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L34) 

> def session_id

For Sauce Labs reporting. Returns the current session id.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] 

--

##### [xpath](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L42) 

> def xpath(xpath_str)

Returns the first element that matches the provided xpath.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] xpath_str - the XPath string

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] 

--

##### [xpaths](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L50) 

> def xpaths(xpath_str)

Returns all elements that match the provided xpath.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] xpath_str - the XPath string

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<Element>] 

--

##### [result](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L61) 

> def result

Returns the value of attribute result

--

##### [initialize](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L63) 

> def initialize



__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[CountElements] a new instance of CountElements

--

##### [reset](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L67) 

> def reset



--

##### [start_element](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L72) 

> def start_element(name, attrs = [], driver = $driver)

http://nokogiri.org/Nokogiri/XML/SAX/Document.html

--

##### [formatted_result](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L78) 

> def formatted_result



--

##### [get_page_class](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L97) 

> def get_page_class

Returns a string of class counts of visible elements.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] 

--

##### [page_class](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L122) 

> def page_class

Count all classes on screen and print to stdout.
Useful for appium_console.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[nil] 

--

##### [px_to_window_rel](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L133) 

> def px_to_window_rel(opts = {}, driver = $driver)

Converts pixel values to window relative values

--

##### [xml_keys](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L152) 

> def xml_keys(target)

Search strings.xml's values for target.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] target - the target to search for in strings.xml values

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array] 

--

##### [xml_values](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L160) 

> def xml_values(target)

Search strings.xml's keys for target.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] target - the target to search for in strings.xml keys

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array] 

--

##### [resolve_id](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L168) 

> def resolve_id(id)

Resolve id in strings.xml and return the value.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] id - the id to resolve

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] 

--

##### [filter](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L175) 

> def filter

Returns the value of attribute filter

--

##### [filter=](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L178) 

> def filter=(value)

convert to string to support symbols

--

##### [initialize](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L184) 

> def initialize



__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[HTMLElements] a new instance of HTMLElements

--

##### [reset](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L189) 

> def reset



--

##### [result](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L195) 

> def result



--

##### [start_element](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L211) 

> def start_element(name, attrs = [])



--

##### [end_element](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L220) 

> def end_element(name)



--

##### [characters](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/helper.rb#L226) 

> def characters(chars)



--

##### [DEFAULT_HEADERS](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/http_client.rb#L8) 

> DEFAULT_HEADERS = { 'Accept' => CONTENT_TYPE, 'User-Agent' => "appium/ruby_lib/#{::Appium::VERSION}" }.freeze

Default HTTP client inherit Appium::Core::Base::Http::Default, but has different DEFAULT_HEADERS

--

##### [pinch](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/multi_touch.rb#L51) 

> def pinch(percentage = 25, auto_perform = true, driver = $driver)

Convenience method for pinching the screen.
Places two fingers at the edges of the screen and brings them together.
Without auto_perform

With driver

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[int] percentage - The percent size by which to shrink the screen when pinched.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[boolean] auto_perform - Whether to perform the action immediately (default true)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Driver] driver - Set a driver to conduct the action. DEfault is global driver($driver)

--

##### [zoom](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/multi_touch.rb#L79) 

> def zoom(percentage = 200, auto_perform = true, driver = $driver)

Convenience method for zooming the screen.
Places two fingers at the edges of the screen and brings them together.
Without auto_perform

With driver

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[int] percentage - The percent size by which to shrink the screen when pinched.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[boolean] auto_perform - Whether to perform the action immediately (default true)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Driver] driver - Set a driver to conduct the action. DEfault is global driver($driver)

--

##### [initialize](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/multi_touch.rb#L84) 

> def initialize(driver = $driver)

self

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[MultiTouch] a new instance of MultiTouch

--

##### [COMPLEX_ACTIONS](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/touch_actions.rb#L33) 

> COMPLEX_ACTIONS = ::Appium::Core::TouchAction::COMPLEX_ACTIONS



--

##### [initialize](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/common/touch_actions.rb#L47) 

> def initialize(driver = $driver)



__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[TouchAction] a new instance of TouchAction

--

##### [for](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/ios.rb#L15) ios

> def self.for(target)



--

##### [UIAStaticText](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/text.rb#L4) ios

> UIAStaticText = 'UIAStaticText'.freeze



--

##### [XCUIElementTypeStaticText](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/text.rb#L5) ios

> XCUIElementTypeStaticText = 'XCUIElementTypeStaticText'.freeze



--

##### [static_text_class](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/text.rb#L8) ios

> def static_text_class



__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] Class name for text

--

##### [text](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/text.rb#L16) ios

> def text(value)

Find the first UIAStaticText|XCUIElementTypeStaticText that contains value or by index.
If int then the UIAStaticText|XCUIElementTypeStaticText at that index is returned.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String, Integer] value - the value to find.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[UIAStaticText|XCUIElementTypeStaticText] 

--

##### [texts](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/text.rb#L25) ios

> def texts(value = false)

Find all UIAStaticTexts|XCUIElementTypeStaticTexts containing value.
If value is omitted, all UIAStaticTexts|XCUIElementTypeStaticTexts are returned

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<UIAStaticText|XCUIElementTypeStaticText>] 

--

##### [first_text](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/text.rb#L32) ios

> def first_text

Find the first UIAStaticText|XCUIElementTypeStaticText.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[UIAStaticText|XCUIElementTypeStaticText] 

--

##### [last_text](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/text.rb#L38) ios

> def last_text

Find the last UIAStaticText|XCUIElementTypeStaticText.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[UIAStaticText|XCUIElementTypeStaticText] 

--

##### [text_exact](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/text.rb#L45) ios

> def text_exact(value)

Find the first UIAStaticText|XCUIElementTypeStaticText that exactly matches value.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to match exactly

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[UIAStaticText|XCUIElementTypeStaticText] 

--

##### [texts_exact](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/text.rb#L52) ios

> def texts_exact(value)

Find all UIAStaticTexts|XCUIElementTypeStaticTexts that exactly match value.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to match exactly

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<UIAStaticText|XCUIElementTypeStaticText>] 

--

##### [filter](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L5) ios

> def filter

Returns the value of attribute filter

--

##### [filter=](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L5) ios

> def filter=(value)

Sets the attribute filter

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;value - the value to set the attribute filter to.

--

##### [start_element](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L7) ios

> def start_element(type, attrs = [])



--

##### [ios_password](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L44) ios

> def ios_password(length = 1)

iOS only. On Android uiautomator always returns an empty string for EditText password.

Password character returned from value of UIASecureTextField

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Integer] length - the length of the password to generate

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] the returned string is of size length

--

##### [page](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L60) ios

> def page(opts = {})

Prints a string of interesting elements to the console.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Hash] visible - a customizable set of options

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Hash] class - a customizable set of options

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[void] 

--

##### [source_window](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L84) ios

> def source_window(_window_number = nil)

Gets the JSON source of window number

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[JSON] 

--

##### [id](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L92) ios

> def id(id)

Find by id

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] id - the id to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] 

--

##### [ele_index](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L100) ios

> def ele_index(class_name, index)

Get the element of type class_name at matching index.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] class_name - the class name to find

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Integer] index - the index

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] 

--

##### [find_ele_by_attr](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L128) ios

> def find_ele_by_attr(class_name, attr, value)

Find the first element exactly matching class and attribute value.
Note: Uses XPath
Note: For XCUITest, this method return ALL elements include displayed or not displayed elements.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] class_name - the class name to search for

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] attr - the attribute to inspect

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the expected value of the attribute

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] 

--

##### [find_eles_by_attr](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L139) ios

> def find_eles_by_attr(class_name, attr, value)

Find all elements exactly matching class and attribute value.
Note: Uses XPath
Note: For XCUITest, this method return ALL elements include displayed or not displayed elements.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] class_name - the class name to match

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] attr - the attribute to compare

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value of the attribute that the element must have

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<Element>] 

--

##### [find_ele_by_predicate](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L152) ios

> def find_ele_by_predicate(class_name: '*', value:)

Find the first element exactly matching attribute case insensitive value.
Note: Uses Predicate

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the expected value of the attribute

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] 

--

##### [find_eles_by_predicate](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L163) ios

> def find_eles_by_predicate(class_name: '*', value:)

Find all elements exactly matching attribute case insensitive value.
Note: Uses Predicate

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value of the attribute that the element must have

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] class_name - the tag name to match

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<Element>] 

--

##### [find_ele_by_attr_include](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L179) ios

> def find_ele_by_attr_include(class_name, attr, value)

Get the first tag by attribute that exactly matches value.
Note: Uses XPath

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] class_name - the tag name to match

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] attr - the attribute to compare

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value of the attribute that the element must include

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] the element of type tag who's attribute includes value

--

##### [find_eles_by_attr_include](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L189) ios

> def find_eles_by_attr_include(class_name, attr, value)

Get tags by attribute that include value.
Note: Uses XPath

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] class_name - the tag name to match

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] attr - the attribute to compare

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value of the attribute that the element must include

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<Element>] the elements of type tag who's attribute includes value

--

##### [find_ele_by_predicate_include](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L197) ios

> def find_ele_by_predicate_include(class_name: '*', value:)

Get the first elements that include insensitive value.
Note: Uses Predicate

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value of the attribute that the element must include

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] the element of type tag who's attribute includes value

--

##### [find_eles_by_predicate_include](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L208) ios

> def find_eles_by_predicate_include(class_name: '*', value:)

Get elements that include case insensitive value.
Note: Uses Predicate

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value of the attribute that the element must include

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] class_name - the tag name to match

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<Element>] the elements of type tag who's attribute includes value

--

##### [first_ele](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L221) ios

> def first_ele(class_name)

Get the first tag that matches class_name

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] class_name - the tag to match

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] 

--

##### [last_ele](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L228) ios

> def last_ele(class_name)

Get the last tag that matches class_name

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] class_name - the tag to match

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] 

--

##### [tag](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L236) ios

> def tag(class_name)

Returns the first **visible** element matching class_name

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] class_name - the class_name to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] 

--

##### [tags](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L244) ios

> def tags(class_name)

Returns all visible elements matching class_name

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] class_name - the class_name to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] 

--

##### [tags_include](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L255) ios

> def tags_include(class_names:, value: nil)

Returns all visible elements matching class_names and value
This method calls find_element/s and element.value/text many times.
So, if you set many class_names, this method's performance become worse.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array[String]] class_names - the class_names to search for

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array[Element]] 

--

##### [tags_exact](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L270) ios

> def tags_exact(class_names:, value: nil)

Returns all visible elements matching class_names and value.
This method calls find_element/s and element.value/text many times.
So, if you set many class_names, this method's performance become worse.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array[String]] class_names - the class_names to search for

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array[Element]] 

--

##### [ele_by_json_visible_contains](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L307) ios

> def ele_by_json_visible_contains(element, value)

Find the first element that contains value.
For Appium(automation name), not XCUITest

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] element - the class name for the element

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] 

--

##### [eles_by_json_visible_contains](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L316) ios

> def eles_by_json_visible_contains(element, value)

Find all elements containing value
For Appium(automation name), not XCUITest

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] element - the class name for the element

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<Element>] 

--

##### [ele_by_json_visible_exact](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L346) ios

> def ele_by_json_visible_exact(element, value)

Find the first element exactly matching value
For Appium(automation name), not XCUITest

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] element - the class name for the element

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] 

--

##### [eles_by_json_visible_exact](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L355) ios

> def eles_by_json_visible_exact(element, value)

Find all elements exactly matching value
For Appium(automation name), not XCUITest

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] element - the class name for the element

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] 

--

##### [_all_pred](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L364) ios

> def _all_pred(opts)

predicate - the predicate to evaluate on the main app

visible - if true, only visible elements are returned. default true

--

##### [ele_with_pred](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L377) ios

> def ele_with_pred(opts)

returns element matching predicate contained in the main app

predicate - the predicate to evaluate on the main app

visible - if true, only visible elements are returned. default true

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] 

--

##### [eles_with_pred](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L388) ios

> def eles_with_pred(opts)

returns elements matching predicate contained in the main app

predicate - the predicate to evaluate on the main app

visible - if true, only visible elements are returned. default true

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<Element>] 

--

##### [source](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L394) ios

> def source

Prints xml of the current page

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[void] 

--

##### [_validate_object](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L398) ios

> def _validate_object(*objects)



--

##### [_by_json](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L447) ios

> def _by_json(opts)

For Appium(automation name), not XCUITest
typeArray - array of string types to search for. Example: ["UIAStaticText"]
onlyFirst - boolean. returns only the first result if true. Example: true
onlyVisible - boolean. returns only visible elements if true. Example: true
target - string. the target value to search for. Example: "Buttons, Various uses of UIButton"
substring - boolean. matches on substrings if true otherwise an exact mathc is required. Example: true
insensitive - boolean. ignores case sensitivity if true otherwise it's case sensitive. Example: true

opts = {
  typeArray: ["UIAStaticText"],
  onlyFirst: true,
  onlyVisible: true,
  name: {
    target: "Buttons, Various uses of UIButton",
    substring: false,
    insensitive: false,
  },
  label: {
    target: "Buttons, Various uses of UIButton",
    substring: false,
    insensitive: false,
  },
  value: {
    target: "Buttons, Various uses of UIButton",
    substring: false,
    insensitive: false,
  }
}

--

##### [eles_by_json](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L497) ios

> def eles_by_json(opts)

For Appium(automation name), not XCUITest
example usage:

eles_by_json({
  typeArray: ["UIAStaticText"],
  onlyVisible: true,
  name: {
    target: "Buttons, Various uses of UIButton",
    substring: false,
    insensitive: false,
  },
})

--

##### [ele_by_json](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L503) ios

> def ele_by_json(opts)

see eles_by_json

--

##### [get_source](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/common/helper.rb#L513) ios

> def get_source

Returns XML string for the current page
Same as driver.page_source

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] 

--

##### [alert_accept](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/alert.rb#L5) ios

> def alert_accept

Accept the alert.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[void] 

--

##### [alert_dismiss](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/alert.rb#L13) ios

> def alert_dismiss

Dismiss the alert.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[void] 

--

##### [UIAButton](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/button.rb#L4) ios

> UIAButton = 'UIAButton'.freeze



--

##### [XCUIElementTypeButton](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/button.rb#L5) ios

> XCUIElementTypeButton = 'XCUIElementTypeButton'.freeze



--

##### [button_class](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/button.rb#L8) ios

> def button_class



__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] Class name for button

--

##### [button](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/button.rb#L16) ios

> def button(value)

Find the first UIAButton|XCUIElementTypeButton that contains value or by index.
If int then the UIAButton|XCUIElementTypeButton at that index is returned.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String, Integer] value - the value to exactly match.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[UIAButton|XCUIElementTypeButton] 

--

##### [buttons](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/button.rb#L26) ios

> def buttons(value = false)

Find all UIAButtons|XCUIElementTypeButtons containing value.
If value is omitted, all UIAButtons|XCUIElementTypeButtons are returned.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<UIAButton|XCUIElementTypeButton>] 

--

##### [first_button](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/button.rb#L33) ios

> def first_button

Find the first UIAButton|XCUIElementTypeButton.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[UIAButton|XCUIElementTypeButton] 

--

##### [last_button](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/button.rb#L41) ios

> def last_button

TODO: add documentation regarding previous element.
      Previous UIAElement is differ from UIAButton|XCUIElementTypeButton. So, the results are different.
Find the last UIAButton|XCUIElementTypeButton.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[UIAButton|XCUIElementTypeButton] 

--

##### [button_exact](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/button.rb#L48) ios

> def button_exact(value)

Find the first UIAButton|XCUIElementTypeButton that exactly matches value.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to match exactly

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[UIAButton|XCUIElementTypeButton] 

--

##### [buttons_exact](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/button.rb#L55) ios

> def buttons_exact(value)

Find all UIAButtons|XCUIElementTypeButtons that exactly match value.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to match exactly

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<UIAButton|XCUIElementTypeButton>] 

--

##### [find](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/generic.rb#L6) ios

> def find(value)

Find the first element containing value

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] 

--

##### [finds](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/generic.rb#L13) ios

> def finds(value)

Find all elements containing value

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<Element>] 

--

##### [find_exact](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/generic.rb#L20) ios

> def find_exact(value)

Find the first element exactly matching value

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] 

--

##### [finds_exact](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/generic.rb#L27) ios

> def finds_exact(value)

Find all elements exactly matching value

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<Element>] 

--

##### [raise_error_if_no_element](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/generic.rb#L33) ios

> def raise_error_if_no_element(element)



--

##### [select_visible_elements](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/generic.rb#L40) ios

> def select_visible_elements(elements)

Return visible elements.

--

##### [for](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/bridge.rb#L7) ios

> def self.for(target)



--

##### [last_ele](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/helper.rb#L26) ios

> def last_ele(class_name)

Get the last tag that matches class_name

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] class_name - the tag to match

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] 

--

##### [tag](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/helper.rb#L36) ios

> def tag(class_name)

Returns the first **visible** element matching class_name

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] class_name - the class_name to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] 

--

##### [tags](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/helper.rb#L44) ios

> def tags(class_name)

Returns all visible elements matching class_name

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] class_name - the class_name to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] 

--

##### [tags_include](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/helper.rb#L56) ios

> def tags_include(class_names:, value: nil)

Returns all visible elements matching class_names and value
This method calls find_element/s and element.value/text many times.
So, if you set many class_names, this method's performance become worse.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array[String]] class_names - the class_names to search for

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array[Element]] 

--

##### [tags_exact](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/helper.rb#L79) ios

> def tags_exact(class_names:, value: nil)

Returns all visible elements matching class_names and value.
This method calls find_element/s and element.value/text many times.
So, if you set many class_names, this method's performance become worse.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array[String]] class_names - the class_names to search for

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array[Element]] 

--

##### [UIATextField](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/textfield.rb#L3) ios

> UIATextField = 'UIATextField'.freeze



--

##### [UIASecureTextField](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/textfield.rb#L4) ios

> UIASecureTextField = 'UIASecureTextField'.freeze



--

##### [XCUIElementTypeTextField](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/textfield.rb#L6) ios

> XCUIElementTypeTextField = 'XCUIElementTypeTextField'.freeze



--

##### [XCUIElementTypeSecureTextField](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/textfield.rb#L7) ios

> XCUIElementTypeSecureTextField = 'XCUIElementTypeSecureTextField'.freeze



--

##### [text_field_class](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/textfield.rb#L10) ios

> def text_field_class



__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] Class name for text field

--

##### [secure_text_field_class](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/textfield.rb#L15) ios

> def secure_text_field_class



__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] Class name for secure text field

--

##### [textfield](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/textfield.rb#L24) ios

> def textfield(value)

Find the first TextField that contains value or by index.
Note: Uses XPath
If int then the TextField at that index is returned.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String, Integer] value - the text to match exactly.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[TextField] 

--

##### [textfields](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/textfield.rb#L42) ios

> def textfields(value = false)

Find all TextFields containing value.
If value is omitted, all TextFields are returned.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<TextField>] 

--

##### [first_textfield](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/textfield.rb#L49) ios

> def first_textfield

Find the first TextField.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[TextField] 

--

##### [last_textfield](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/textfield.rb#L55) ios

> def last_textfield

Find the last TextField.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[TextField] 

--

##### [textfield_exact](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/textfield.rb#L64) ios

> def textfield_exact(value)

Find the first TextField that exactly matches value.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to match exactly

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[TextField] 

--

##### [textfields_exact](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/textfield.rb#L71) ios

> def textfields_exact(value)

Find all TextFields that exactly match value.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to match exactly

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<TextField>] 

--

##### [_textfield_visible](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/textfield.rb#L78) ios

> def _textfield_visible

Appium

--

##### [_textfield_exact_string](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/textfield.rb#L83) ios

> def _textfield_exact_string(value)

Appium

--

##### [_textfield_contains_string](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/element/textfield.rb#L90) ios

> def _textfield_contains_string(value)

Appium

--

##### [static_text_class](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/text.rb#L9) ios

> def static_text_class



__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] Class name for text

--

##### [text](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/text.rb#L17) ios

> def text(value)

Find the first UIAStaticText|XCUIElementTypeStaticText that contains value or by index.
If int then the UIAStaticText|XCUIElementTypeStaticText at that index is returned.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String, Integer] value - the value to find.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[UIAStaticText|XCUIElementTypeStaticText] 

--

##### [texts](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/text.rb#L26) ios

> def texts(value = false)

Find all UIAStaticTexts|XCUIElementTypeStaticTexts containing value.
If value is omitted, all UIAStaticTexts|XCUIElementTypeStaticTexts are returned

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<UIAStaticText|XCUIElementTypeStaticText>] 

--

##### [first_text](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/text.rb#L34) ios

> def first_text

Find the first UIAStaticText|XCUIElementTypeStaticText.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[UIAStaticText|XCUIElementTypeStaticText] 

--

##### [last_text](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/text.rb#L40) ios

> def last_text

Find the last UIAStaticText|XCUIElementTypeStaticText.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[UIAStaticText|XCUIElementTypeStaticText] 

--

##### [text_exact](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/text.rb#L47) ios

> def text_exact(value)

Find the first UIAStaticText|XCUIElementTypeStaticText that exactly matches value.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to match exactly

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[UIAStaticText|XCUIElementTypeStaticText] 

--

##### [texts_exact](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/text.rb#L54) ios

> def texts_exact(value)

Find all UIAStaticTexts|XCUIElementTypeStaticTexts that exactly match value.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to match exactly

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<UIAStaticText|XCUIElementTypeStaticText>] 

--

##### [button_class](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/button.rb#L9) ios

> def button_class



__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] Class name for button

--

##### [button](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/button.rb#L17) ios

> def button(value)

Find the first UIAButton|XCUIElementTypeButton that contains value or by index.
If int then the UIAButton|XCUIElementTypeButton at that index is returned.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String, Integer] value - the value to exactly match.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[UIAButton|XCUIElementTypeButton] 

--

##### [buttons](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/button.rb#L27) ios

> def buttons(value = false)

Find all UIAButtons|XCUIElementTypeButtons containing value.
If value is omitted, all UIAButtons|XCUIElementTypeButtons are returned.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<UIAButton|XCUIElementTypeButton>] 

--

##### [first_button](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/button.rb#L35) ios

> def first_button

Find the first UIAButton|XCUIElementTypeButton.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[UIAButton|XCUIElementTypeButton] 

--

##### [last_button](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/button.rb#L43) ios

> def last_button

TODO: add documentation regarding previous element.
      Previous UIAElement is differ from UIAButton|XCUIElementTypeButton. So, the results are different.
Find the last UIAButton|XCUIElementTypeButton.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[UIAButton|XCUIElementTypeButton] 

--

##### [button_exact](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/button.rb#L50) ios

> def button_exact(value)

Find the first UIAButton|XCUIElementTypeButton that exactly matches value.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to match exactly

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[UIAButton|XCUIElementTypeButton] 

--

##### [buttons_exact](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/button.rb#L57) ios

> def buttons_exact(value)

Find all UIAButtons|XCUIElementTypeButtons that exactly match value.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to match exactly

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<UIAButton|XCUIElementTypeButton>] 

--

##### [find](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/generic.rb#L8) ios

> def find(value)

Find the first element containing value

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] 

--

##### [finds](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/generic.rb#L15) ios

> def finds(value)

Find all elements containing value

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<Element>] 

--

##### [find_exact](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/generic.rb#L23) ios

> def find_exact(value)

Find the first element exactly matching value

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] 

--

##### [finds_exact](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/generic.rb#L30) ios

> def finds_exact(value)

Find all elements exactly matching value

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<Element>] 

--

##### [raise_error_if_no_element](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/generic.rb#L37) ios

> def raise_error_if_no_element(element)



--

##### [select_visible_elements](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/generic.rb#L44) ios

> def select_visible_elements(elements)

Return visible elements.

--

##### [swipe](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/command/gestures.rb#L11) ios

> def swipe(direction:, element: nil)



__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[string] direction - Either 'up', 'down', 'left' or 'right'.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Hash] opts - a customizable set of options

--

##### [scroll](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/command/gestures.rb#L29) ios

> def scroll(direction:, name: nil, element: nil, to_visible: nil, predicate_string: nil)



__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[string] direction - Either 'up', 'down', 'left' or 'right'.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Hash] opts - a customizable set of options

--

##### [pinch](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/command/gestures.rb#L48) ios

> def pinch(scale:, velocity: 1.0, element: nil)



__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[scale] scale - X tap coordinate of type float. Mandatory parameter

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[float] velocity - Y tap coordinate of type float. Mandatory parameter

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Hash] opts - a customizable set of options

--

##### [double_tap](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/command/gestures.rb#L63) ios

> def double_tap(x: nil, y: nil, element: nil)



__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[float] x - X Screen x tap coordinate of type float. Mandatory parameter only if element is not set

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[float] y - Y Screen y tap coordinate of type float. Mandatory parameter only if element is not set

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Hash] opts - a customizable set of options

--

##### [touch_and_hold](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/command/gestures.rb#L80) ios

> def touch_and_hold(x: nil, y: nil, element: nil, duration: 1.0)



__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[float] x - Screen x long tap coordinate of type float. Mandatory parameter only if element is not set

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[float] y - Screen y long tap coordinate of type float. Mandatory parameter only if element is not set

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Float] duration - The float duration of press action in seconds. Mandatory parameter

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Hash] opts - a customizable set of options

--

##### [two_finger_tap](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/command/gestures.rb#L93) ios

> def two_finger_tap(element:)



__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] element - Element to long tap on.

```ruby
two_finger_tap element: find_element(:accessibility_id, "some item")
```

--

##### [tap](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/command/gestures.rb#L108) ios

> def tap(x:, y:, element: nil)



__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[float] x - X tap coordinate of type float. Mandatory parameter

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[float] y - Y tap coordinate of type float. Mandatory parameter

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Hash] opts - a customizable set of options

--

##### [drag_from_to_for_duration](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/command/gestures.rb#L128) ios

> def drag_from_to_for_duration(from_x:, from_y:, to_x:, to_y:, duration: 1.0, element: nil)

rubocop:disable Metrics/ParameterLists

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[float] duration - Float number of seconds in range [0.5, 60]. How long the tap gesture at starting
drag point should be before to start dragging. Mandatory parameter

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[float] from_x - The x coordinate of starting drag point (type float). Mandatory parameter

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[float] from_y - The y coordinate of starting drag point (type float). Mandatory parameter

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[float] to_x - The x coordinate of ending drag point (type float). Mandatory parameter

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[float] to_y - The y coordinate of ending drag point (type float). Mandatory parameter

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Hash] opts - a customizable set of options

--

##### [select_picker_wheel](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/command/gestures.rb#L145) ios

> def select_picker_wheel(element:, order:, offset: nil)

https://github.com/facebook/WebDriverAgent/pull/523
https://github.com/appium/appium-xcuitest-driver/pull/420

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] order - The order to move picker to. "next" or "previous".

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Element] element - Element id to perform select picker wheel on.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Hash] opts - a customizable set of options

--

##### [alert](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/command/gestures.rb#L163) ios

> def alert(action:, button_label: nil)



__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] action - The following actions are supported: accept, dismiss and getButtons. Mandatory parameter

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] button_label - The label text of an existing alert button to click on.
This is an optional parameter and is only valid in combination with accept and dismiss actions.

--

##### [text_field_class](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/textfield.rb#L9) ios

> def text_field_class



__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] Class name for text field

--

##### [secure_text_field_class](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/textfield.rb#L14) ios

> def secure_text_field_class



__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] Class name for secure text field

--

##### [textfield](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/textfield.rb#L23) ios

> def textfield(value)

Find the first TextField that contains value or by index.
Note: Uses XPath
If int then the TextField at that index is returned.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String, Integer] value - the text to match exactly.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[TextField] 

--

##### [textfields](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/textfield.rb#L41) ios

> def textfields(value = false)

Find all TextFields containing value.
If value is omitted, all TextFields are returned.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to search for

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<TextField>] 

--

##### [first_textfield](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/textfield.rb#L50) ios

> def first_textfield

Find the first TextField.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[TextField] 

--

##### [last_textfield](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/textfield.rb#L56) ios

> def last_textfield

Find the last TextField.

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[TextField] 

--

##### [textfield_exact](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/textfield.rb#L65) ios

> def textfield_exact(value)

Find the first TextField that exactly matches value.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to match exactly

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[TextField] 

--

##### [textfields_exact](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/element/textfield.rb#L72) ios

> def textfields_exact(value)

Find all TextFields that exactly match value.

__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[String] value - the value to match exactly

__Returns:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Array<TextField>] 

--

##### [set_pasteboard](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/command/pasteboard.rb#L12) ios

> def set_pasteboard(content:, encoding: nil)



__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[string] content - The content of the pasteboard. The previous content is going to be overridden.
The parameter is mandatory

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Hash] opts - a customizable set of options

--

##### [get_pasteboard](https://github.com/appium/ruby_lib/blob/b9b8784697d9fbe73d3883cf42d260f19138d8f5/lib/appium_lib/ios/xcuitest/command/pasteboard.rb#L24) ios

> def get_pasteboard(encoding: nil)



__Parameters:__

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Hash] opts - a customizable set of options

--

