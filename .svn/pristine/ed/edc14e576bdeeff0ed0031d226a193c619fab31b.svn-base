<?php
/**
Plugin Name: Islamic Content Archive For Muslim e-Library
Plugin URI: http://www.muslim-library.com
Description: Our Comprehensive Muslim e-Library endeavors to be a unique comprehensive online store of free downloadable PDF books about Islam, Muslims, and other faiths in many languages.
Version: 1.0
Author: EDC Team (E-Da`wah Committee)
Author URI: http://www.muslim-library.com
License: Free
*/

define('ICA_ML_PATH',plugin_dir_path( __FILE__ ));
define('ICA_ML_URL',plugin_dir_url( __FILE__ ));
define('ICA_ML_Page_SLUG','ica_ml');
define('ICA_ML_Input_SLUG','ica_ml_');
define('ICA_ML_LIB','lib');
define('ICA_ML_DS','/');
define('ICA_ML_CONTROLLERS','controllers');
define('ICA_ML_MODELS','models');
define('ICA_ML_DBTable', 'ica_ml_categories');

define('ICA_ML_Logo_url',ICA_ML_URL.'style'.ICA_ML_DS.'images'.ICA_ML_DS.'logo'.ICA_ML_DS);
define('ICA_ML_Icon_path',ICA_ML_PATH.'style'.ICA_ML_DS.'images'.ICA_ML_DS.'icons'.ICA_ML_DS);
define('ICA_ML_Icon_url',ICA_ML_URL.'style'.ICA_ML_DS.'images'.ICA_ML_DS.'icons'.ICA_ML_DS);
define('ICA_ML_Flags_path',ICA_ML_PATH.'style'.ICA_ML_DS.'images'.ICA_ML_DS.'flags'.ICA_ML_DS);
define('ICA_ML_Flags_url',ICA_ML_URL.'style'.ICA_ML_DS.'images'.ICA_ML_DS.'flags'.ICA_ML_DS);

define('ICA_ML_Controlers_path',ICA_ML_PATH.'controllers'.ICA_ML_DS);
define('ICA_ML_MODELS_path',ICA_ML_PATH.'models'.ICA_ML_DS);
define('ICA_ML_Views_path',ICA_ML_PATH.'views'.ICA_ML_DS);
define('ICA_ML_Layout_path',ICA_ML_PATH.'views'.ICA_ML_DS.'layout'.ICA_ML_DS);
define('ICA_ML_Lang_path',ICA_ML_PATH.'views'.ICA_ML_DS.'lang'.ICA_ML_DS);

function ica_ml_plugin_install(){
	$default_lang = 'eng';
	$source = 'Soucre Link';
	add_option(ICA_ML_Input_SLUG.'language', $default_lang);
	add_option(ICA_ML_Input_SLUG.'source', $source);
	add_option(ICA_ML_Input_SLUG.'cronjobtime', 'everyhour');
	add_option(ICA_ML_Input_SLUG.'version', '1.0');
}
function ica_ml_plugin_uninstall(){
	$options = get_option(ICA_ML_Input_SLUG.'language');
 	if( is_array($options) && $options['uninstall'] === true){
		delete_option(ICA_ML_Input_SLUG.'language');
		delete_option(ICA_ML_Input_SLUG.'source');
		delete_option(ICA_ML_Input_SLUG.'cronjobtime');
		delete_option(ICA_ML_Input_SLUG.'version');
	}
}
register_activation_hook(plugin_basename(__FILE__),'ica_ml_plugin_install'); 
register_deactivation_hook(plugin_basename(__FILE__), 'ica_ml_plugin_uninstall');

include_once(ICA_ML_PATH.'load.php');