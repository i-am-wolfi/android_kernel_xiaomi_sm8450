# SPDX-License-Identifier: GPL-2.0

ccflags-y += -I$(src)

# Subdirectories
obj-y += locking/
obj-y += rcu/
obj-y += sched/walt/
obj-y += trace/

obj-$(CONFIG_MSM_SYSSTATS) += msm_sysstats.o

obj-$(CONFIG_TORTURE_TEST) += torture.o


# --- marble: objs upstream restaurados ---
ifdef CONFIG_GKI_HACKS_TO_FIX
CFLAGS_cred.o = -DANDROID_GKI_VFS_EXPORT_ONLY=VFS_internal_I_am_really_a_filesystem_and_am_NOT_a_driver
endif
ifdef CONFIG_GKI_HACKS_TO_FIX
else
CFLAGS_cred.o = -DANDROID_GKI_VFS_EXPORT_ONLY=""
endif
obj-y += ksysfs.o softirq.o sysctl.o ptrace.o umh.o ksyms_common.o params.o reboot.o resource.o pid.o user.o extable.o smpboot.o sys.o sys_ni.o signal.o cred.o kthread.o fork.o regset.o task_work.o notifier.o nsproxy.o workqueue.o capability.o panic.o exec_domain.o async.o exit.o cpu.o ucount.o range.o
obj-$(CONFIG_USERMODE_DRIVER) += usermode_driver.o
obj-$(CONFIG_MULTIUSER) += groups.o
obj-$(CONFIG_VHOST_TASK) += vhost_task.o
ifdef CONFIG_FUNCTION_TRACER
CFLAGS_REMOVE_irq_work.o = $(CC_FLAGS_FTRACE)
endif
KCOV_INSTRUMENT_softirq.o := n
KCSAN_SANITIZE_softirq.o = n
KCOV_INSTRUMENT_extable.o := n
KCOV_INSTRUMENT_stacktrace.o := n
KCOV_INSTRUMENT_kcov.o := n
KASAN_SANITIZE_kcov.o := n
KCSAN_SANITIZE_kcov.o := n
UBSAN_SANITIZE_kcov.o := n
KMSAN_SANITIZE_kcov.o := n
CFLAGS_kcov.o := $(call cc-option, -fno-conserve-stack) -fno-stack-protector
obj-y += sched/
obj-y += power/
obj-y += printk/
obj-y += irq/
obj-y += livepatch/
obj-y += dma/
obj-y += entry/
obj-$(CONFIG_MODULES) += module/
obj-$(CONFIG_KCMP) += kcmp.o
obj-$(CONFIG_FREEZER) += freezer.o
obj-$(CONFIG_PROFILING) += profile.o
obj-$(CONFIG_STACKTRACE) += stacktrace.o
obj-y += time/
obj-$(CONFIG_FUTEX) += futex/
obj-$(CONFIG_GENERIC_ISA_DMA) += dma.o
obj-$(CONFIG_SMP) += smp.o
ifneq ($(CONFIG_SMP),y)
obj-y += up.o
endif
obj-$(CONFIG_UID16) += uid16.o
obj-$(CONFIG_MODULE_SIG_FORMAT) += module_signature.o
obj-$(CONFIG_KALLSYMS) += kallsyms.o
obj-$(CONFIG_KALLSYMS_SELFTEST) += kallsyms_selftest.o
obj-$(CONFIG_BSD_PROCESS_ACCT) += acct.o
obj-$(CONFIG_VMCORE_INFO) += elfcorehdr.o vmcore_info.o
obj-$(CONFIG_CRASH_RESERVE) += crash_reserve.o
obj-$(CONFIG_KEXEC_CORE) += kexec_core.o
obj-$(CONFIG_CRASH_DUMP) += crash_core.o
obj-$(CONFIG_KEXEC) += kexec.o
obj-$(CONFIG_KEXEC_FILE) += kexec_file.o
obj-$(CONFIG_KEXEC_ELF) += kexec_elf.o
obj-$(CONFIG_BACKTRACE_SELF_TEST) += backtracetest.o
obj-$(CONFIG_COMPAT) += compat.o
obj-$(CONFIG_CGROUPS) += cgroup/
obj-$(CONFIG_UTS_NS) += utsname.o
obj-$(CONFIG_USER_NS) += user_namespace.o
obj-$(CONFIG_PID_NS) += pid_namespace.o
obj-$(CONFIG_IKCONFIG) += configs.o
obj-$(CONFIG_IKHEADERS) += kheaders.o
obj-$(CONFIG_SMP) += stop_machine.o
obj-$(CONFIG_AUDIT) += auditfilter.o audit.o
obj-$(CONFIG_AUDITSYSCALL) += auditsc.o audit_tree.o audit_watch.o audit_fsnotify.o
obj-$(CONFIG_GCOV_KERNEL) += gcov/
obj-$(CONFIG_KCOV) += kcov.o
obj-$(CONFIG_KPROBES) += kprobes.o
obj-$(CONFIG_FAIL_FUNCTION) += fail_function.o
obj-$(CONFIG_KGDB) += debug/
obj-$(CONFIG_DETECT_HUNG_TASK) += hung_task.o
obj-$(CONFIG_LOCKUP_DETECTOR) += watchdog.o
obj-$(CONFIG_HARDLOCKUP_DETECTOR_BUDDY) += watchdog_buddy.o
obj-$(CONFIG_HARDLOCKUP_DETECTOR_PERF) += watchdog_perf.o
obj-$(CONFIG_SECCOMP) += seccomp.o
obj-$(CONFIG_RELAY) += relay.o
obj-$(CONFIG_SYSCTL) += utsname_sysctl.o
obj-$(CONFIG_TASK_DELAY_ACCT) += delayacct.o
obj-$(CONFIG_TASKSTATS) += tsacct.o taskstats.o
obj-$(CONFIG_TRACEPOINTS) += tracepoint.o
obj-$(CONFIG_LATENCYTOP) += latencytop.o
obj-$(CONFIG_IRQ_WORK) += irq_work.o
obj-$(CONFIG_CPU_PM) += cpu_pm.o
obj-$(CONFIG_BPF) += bpf/
obj-$(CONFIG_KCSAN) += kcsan/
obj-$(CONFIG_SHADOW_CALL_STACK) += scs.o
obj-$(CONFIG_HAVE_STATIC_CALL) += static_call.o
obj-$(CONFIG_HAVE_STATIC_CALL_INLINE) += static_call_inline.o
obj-$(CONFIG_CFI_CLANG) += cfi.o
obj-$(CONFIG_PERF_EVENTS) += events/
obj-$(CONFIG_USER_RETURN_NOTIFIER) += user-return-notifier.o
obj-$(CONFIG_PADATA) += padata.o
obj-$(CONFIG_JUMP_LABEL) += jump_label.o
obj-$(CONFIG_CONTEXT_TRACKING) += context_tracking.o
obj-$(CONFIG_HAS_IOMEM) += iomem.o
obj-$(CONFIG_RSEQ) += rseq.o
obj-$(CONFIG_WATCH_QUEUE) += watch_queue.o
obj-$(CONFIG_RESOURCE_KUNIT_TEST) += resource_kunit.o
obj-$(CONFIG_SYSCTL_KUNIT_TEST) += sysctl-test.o
CFLAGS_stackleak.o += $(DISABLE_STACKLEAK_PLUGIN)
obj-$(CONFIG_GCC_PLUGIN_STACKLEAK) += stackleak.o
KASAN_SANITIZE_stackleak.o := n
KCSAN_SANITIZE_stackleak.o := n
KCOV_INSTRUMENT_stackleak.o := n
obj-$(CONFIG_SCF_TORTURE_TEST) += scftorture.o
$(obj)/configs.o: $(obj)/config_data.gz
targets += config_data config_data.gz
$(obj)/config_data.gz: $(obj)/config_data FORCE
	$(call if_changed,gzip)
$(obj)/config_data: $(KCONFIG_CONFIG) FORCE
	$(call filechk,cat)
$(obj)/kheaders.o: $(obj)/kheaders_data.tar.xz
quiet_cmd_genikh = CHK     $(obj)/kheaders_data.tar.xz
      cmd_genikh = $(CONFIG_SHELL) $(srctree)/kernel/gen_kheaders.sh $@
$(obj)/kheaders_data.tar.xz: FORCE
	$(call cmd,genikh)
clean-files := kheaders_data.tar.xz kheaders.md5
