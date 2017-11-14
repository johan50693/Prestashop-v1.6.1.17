# Prestashop-v1.6.1.17
links de interes 
http://doc.prestashop.com/display/PS16/Chapter+3+-+First+steps+-+Accessing+the+web+service+and+listing+customers

https://www.video2brain.com/mx/tutorial/que-son-los-front-controllers-creando-un-controlador

Filtros 
https://datatables.net/examples/advanced_init/

Admincontroller
http://proactive-learning.readthedocs.io/es/latest/php/prestashop/admincontroller.html

libro
https://books.google.co.ve/books?id=BsSiBQAAQBAJ&pg=PT169&lpg=PT169&dq=admin+controller+prestashop&source=bl&ots=JDaT3pE6cp&sig=i_xvFBjJJKeN2n7FPpvmPOj82cg&hl=es-419&sa=X&ved=0ahUKEwiz79PFwKzXAhXCOSYKHdzLCj44ChDoAQhQMAY#v=onepage&q=admin%20controller%20prestashop&f=false

Ejemplos modulos
http://nemops.com/category/tutorials/development/

ajax 
http://doc.prestashop.com/display/PS16/Using+jQuery+and+Ajax

add css
http://nemops.com/creating-new-pages-in-prestashop/#.WgJnX5_iaFM

cursos
https://www.video2brain.com/mx/tutorial/aplicando-js-y-css-a-nuestro-modulo-de-prestashop/comentarios-de-los-usuarios

panel de configuracion del modulo
http://trikendo.com/blog/1-3-creando-un-formulario-de-configuracion-sencillo/

https://www.amauri.eng.br/en/blog/2016/03/developing-a-simple-module-with-crud-for-prestashop/
https://webkul.com/blog/create-and-submit-form-using-renderoptions-in-admin-controller-of-prestashop/

Cargar .tpl en controller
public function initContent()
{
    parent::initContent();

    $smarty = $this->context->smarty;
    // msg and title variables must be assigned before fetching template
    // otherwise they are not recognized in template
    $smarty->assign(array(
        'msg' => $this->msg,
        'title' => $this->title
    ));
    $content = $smarty->fetch(_PS_MODULE_DIR_ . 'pushnotification/views/templates/admin/pushnotificationform.tpl');
    $smarty->assign(array(
        'content' => $this->content . $content
    ));
}

Obtener link para controlador

https://stackoverflow.com/questions/39290553/prestashop-1-6-how-to-create-and-submit-custom-form-using-admin-controller


