iCheck
=======

The admin comes with `iCheck <https://github.com/fronteed/icheck`_ integration
since version 1.0.2. iCheck is a jQuery based replacement for checkbox.

The iCheck is enabled on all ``checkbox`` form elements by default.



Disable icheck on some form elements
-------------------------------------

To disable icheck on some ``checkbox`` form element, set data attribute ``data-sonata-icheck = "false"`` to this form element.

.. code-block:: php

    <?php

    use Sonata\AdminBundle\Form\Type\ModelType;

    protected function configureFormFields(FormMapper $formMapper)
    {
        $formMapper
            ->add('category', ModelType::class, [
                'attr' => [
                    'data-sonata-icheck' => 'false'
                ]
            ])
        ;
    }

.. note::

    You have to use false as string! ``"false"``!